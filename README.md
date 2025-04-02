<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }
        .tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 20px;
        }
        .tab {
            padding: 10px 20px;
            cursor: pointer;
            border: 1px solid #ccc;
            background-color: #f0f0f0;
            margin: 0 5px;
            border-radius: 5px;
        }
        .tab:hover {
            background-color: #ddd;
        }
        .content {
            display: none;
        }
        .active {
            display: block;
        }
    </style>
</head>
<body>
    <h1>YOUR NAME</h1>
    <div class="tabs">
        <div class="tab" onclick="showTab('home')">Home</div>
        <div class="tab" onclick="showTab('about')">About</div>
        <div class="tab" onclick="showTab('gallery')">Gallery</div>
        <div class="tab" onclick="showTab('contact')">Contact</div>
    </div>
    
    <div id="home" class="content active">
        <p>Welcome to my website!</p>
        <img src="https://content.codecademy.com/articles/github-pages-via-web-app/happy-ice-cream.gif" />
    </div>
    
    <div id="about" class="content">
        <p>This is the about page. Here you can write about yourself.</p>
    </div>
    
    <div id="gallery" class="content">
        <p>Check out some cool images!</p>
        <img src="https://via.placeholder.com/150" />
        <img src="https://via.placeholder.com/150" />
    </div>
    
    <div id="contact" class="content">
        <p>Contact me at: example@email.com</p>
    </div>
    
    <script>
        function showTab(tabId) {
            var contents = document.querySelectorAll('.content');
            contents.forEach(content => content.classList.remove('active'));
            document.getElementById(tabId).classList.add('active');
        }
    </script>
</body>
</html>
