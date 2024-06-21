<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Asacom Klodin</title>
    <style>
        body {
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }

        #loading {
            display: flex;
            justify-content: center;
            align-items: center;
            position: fixed;
            width: 100%;
            height: 100%;
            background-color: #ffffff; /* White background */
            color: #4caf50; /* Green text */
            z-index: 1000;
            flex-direction: column;
            opacity: 1;
            animation: fadeinout 5s forwards;
        }

        #loading h1 {
            font-size: 2.5em;
            margin: 0;
        }

        #loading p {
            font-size: 1.25em;
            margin: 10px 0 0;
            font-style: italic;
        }

        @keyframes fadeinout {
            0%, 100% { opacity: 0; }
            50% { opacity: 1; }
        }

        #main-content {
            display: none;
        }

        header {
            background-color: #4caf50; /* Green background */
            color: #fff;
            padding: 30px 0;
            text-align: center;
        }

        header h1 {
            font-size: 2.5em;
            margin: 0;
            font-weight: normal;
        }

        header p.slogan {
            font-size: 1em;
            margin: 10px 0 0;
            font-style: italic;
            color: #ffffff; /* White */
        }

        nav {
            background-color: #cfd8dc; /* Light background */
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
            justify-content: center;
        }

        nav ul li {
            margin: 0;
        }

        nav ul li a {
            color: #333;
            text-decoration: none;
            padding: 20px 30px;
            display: block;
            transition: background-color 0.3s ease, color 0.3s ease;
            font-size: 1.2em;
        }

        nav ul li a:hover {
            background-color: #4caf50; /* Green background */
            color: #fff;
        }

        main {
            padding: 60px 20px;
            text-align: center;
        }

        main h2 {
            font-size: 2em;
            margin-bottom: 20px;
            color: #333;
        }

        main p {
            font-size: 1.2em;
            margin-bottom: 40px;
            color: #757575;
        }

        footer {
            background-color: #4caf50; /* Green background */
            color: #fff;
            text-align: center;
            padding: 15px 0;
            position: fixed;
            width: 100%;
            bottom: 0;
            box-shadow: 0 -2px 8px rgba(0, 0, 0, 0.1);
        }

        footer p {
            margin: 0;
        }

        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
            }

            nav ul li a {
                padding: 15px 20px;
            }
        }
    </style>
</head>
<body>
    <div id="loading">
        <h1>Asacom Klodin</h1>
        <p class="slogan">...elevate your style, embrace your individuality!</p>
    </div>
    <div id="main-content">
        <header>
            <h1>Welcome to Asacom Klodin</h1>
            <p class="slogan">Elevate your style, embrace your individuality</p>
        </header>
        <nav>
            <ul>
                <li><a href="casual.html" class="category-link" data-category="Casual">Casual</a></li>
                <li><a href="formal.html" class="category-link" data-category="Formal">Formal</a></li>
                <li><a href="evening.html" class="category-link" data-category="Evening">Evening</a></li>
                <li><a href="traditional.html" class="category-link" data-category="Traditional">Traditional</a></li>
                <li><a href="custom.html" class="category-link" data-category="Custom">Custom</a></li>
            </ul>
        </nav>
        <main>
            <h2>Choose a Style Category</h2>
            <p>Click on the categories above to view various dress templates.</p>
        </main>
        <footer>
            <p>&copy; 2024 Asacom Klodin. All rights reserved.</p>
        </footer>
    </div>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            setTimeout(() => {
                document.getElementById('loading').style.display = 'none';
                document.getElementById('main-content').style.display = 'block';
            }, 5000); // 5 seconds

            const categoryLinks = document.querySelectorAll('.category-link');

            categoryLinks.forEach(link => {
                link.addEventListener('click', (event) => {
                    const category = event.target.getAttribute('data-category');
                    alert(`You clicked on the ${category} category.`);
                });
            });
        });
    </script>
</body>
</html>
