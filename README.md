<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your GitHub Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');
        
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #0e0e0e;
            color: #333;
            overflow-x: hidden;
            position: relative;
        }
        header {
            background: linear-gradient(90deg, #ff8a00, #e52e71);
            color: white;
            padding: 1rem 0;
            text-align: center;
            font-size: 2rem;
            z-index: 10;
            position: relative;
            animation: slide-down 1s ease-out;
        }
        @keyframes slide-down {
            from {
                transform: translateY(-100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }
        .container {
            width: 80%;
            margin: 2rem auto;
            text-align: center;
            z-index: 10;
            position: relative;
        }
        .profile {
            display: inline-block;
            margin-bottom: 2rem;
            animation: fade-in 2s ease-in;
        }
        @keyframes fade-in {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
        .profile img {
            border-radius: 50%;
            width: 150px;
            height: 150px;
            object-fit: cover;
        }
        .profile h1 {
            margin: 1rem 0 0.5rem;
            font-weight: 700;
            color: white;
        }
        .profile p {
            font-size: 1.1rem;
            color: #cccccc;
        }
        .socials {
            display: flex;
            justify-content: center;
            margin-top: 1rem;
        }
        .socials a {
            margin: 0 1rem;
            color: #4A90E2;
            text-decoration: none;
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        .socials a:hover {
            color: #ff8a00;
        }
        .repos {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 1rem;
            animation: slide-up 1.5s ease-out;
        }
        @keyframes slide-up {
            from {
                transform: translateY(100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }
        .repo {
            background-color: #fff;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            text-align: left;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .repo:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .repo h2 {
            font-size: 1.2rem;
            margin: 0 0 0.5rem;
            color: #e52e71;
        }
        .repo p {
            font-size: 0.9rem;
            color: #666;
        }
        footer {
            text-align: center;
            padding: 1rem 0;
            background: linear-gradient(90deg, #e52e71, #ff8a00);
            color: white;
            margin-top: 2rem;
            animation: slide-up 2s ease-out;
            z-index: 10;
            position: relative;
        }
        .binary-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: 0;
        }
        .binary {
            position: absolute;
            color: rgba(0, 255, 0, 0.1); /* Change this color to your preferred binary color */
            font-size: 16px;
            animation: move 10s linear infinite;
        }
        @keyframes move {
            from {
                top: -100px;
            }
            to {
                top: 100vh;
            }
        }
    </style>
</head>
<body>
    <header>
        Welcome to My GitHub Profile
    </header>
    <div class="binary-background" id="binary-background"></div>
    <div class="container">
        <div class="profile">
            <img src="profil.jpg" alt="Profile Picture">
            <h1>Your Name</h1>
            <p>Hello! I'm [Your Name], a passionate [Your Profession] based in [Your Location]. I love [Your Interests/Hobbies].</p>
        </div>
        <div class="socials">
            <a href="https://twitter.com/yourusername" target="_blank">Twitter</a>
            <a href="https://www.linkedin.com/in/yourusername/" target="_blank">LinkedIn</a>
            <a href="https://github.com/yourusername" target="_blank">GitHub</a>
        </div>
        <div class="repos">
            <div class="repo">
                <h2>Repo 1</h2>
                <p>Description of the repository. Technologies used: HTML, CSS, JavaScript.</p>
            </div>
            <div class="repo">
                <h2>Repo 2</h2>
                <p>Description of the repository. Technologies used: Python, Flask.</p>
            </div>
            <div class="repo">
                <h2>Repo 3</h2>
                <p>Description of the repository. Technologies used: Java, Spring Boot.</p>
            </div>
            <!-- Add more repositories as needed -->
        </div>
    </div>
    <footer>
        &copy; 2024 Your Name. All rights reserved.
    </footer>
    <script>
        const binaryBackground = document.getElementById('binary-background');
        const binaryChars = '01';
        const binaryArray = [];

        for (let i = 0; i < 200; i++) {
            const binaryElement = document.createElement('div');
            binaryElement.classList.add('binary');
            binaryElement.style.left = `${Math.random() * 100}vw`;
            binaryElement.style.animationDuration = `${Math.random() * 10 + 5}s`;
            binaryElement.textContent = binaryChars[Math.floor(Math.random() * binaryChars.length)];
            binaryBackground.appendChild(binaryElement);
            binaryArray.push(binaryElement);
        }
    </script>
</body>
</html>
