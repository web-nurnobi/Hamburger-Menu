# Hamburger-Menu
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .menu-line {
            width: 30px;
            height: 24px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            cursor: pointer;
        }

        .menu-single-line {
            width: 100%;
            height: 3px;
            background-color: black;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        /* Toggle Animation */
        .menu-line.active .menu-single-line:nth-child(1) {
            transform: rotate(45deg) translate(6px, 6px);
        }

        .menu-line.active .menu-single-line:nth-child(2) {
            opacity: 0;
        }

        .menu-line.active .menu-single-line:nth-child(3) {
            transform: rotate(-45deg) translate(8px, -8px);
        }
    </style>
</head>
<body>
    <div class="menu-line" id="menuBtn">
        <div class="menu-single-line"></div>
        <div class="menu-single-line"></div>
        <div class="menu-single-line"></div>
    </div>
    <script>
        const menuBtn = document.getElementById("menuBtn");

        menuBtn.addEventListener("click", () => {
            menuBtn.classList.toggle("active");
        });
    </script>
</body>

</html>
