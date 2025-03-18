<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Hollowed Arcana</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: url('dark_library_background.jpg') no-repeat center center fixed;
            background-size: cover;
            color: #e0d6b9;
            font-family: 'Garamond', serif;
            text-align: center;
            overflow-x: hidden;
        }
        .intro {
            font-size: 24px;
            padding: 50px;
        }
        .pillars-container {
            display: flex;
            justify-content: center;
            gap: 100px;
            margin-top: 50px;
        }
        .pillar {
            width: 150px;
            height: 300px;
            background: url('pillar_texture.png') no-repeat center;
            background-size: cover;
            position: relative;
            cursor: pointer;
            transition: transform 0.3s ease-in-out;
        }
        .pillar:hover {
            transform: scale(1.1);
        }
        .statue {
            width: 100px;
            height: 150px;
            background: url('statue.png') no-repeat center;
            background-size: cover;
            position: absolute;
            top: -130px;
            left: 25px;
        }
        #library-scene {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('library_interior.jpg') no-repeat center;
            background-size: cover;
            opacity: 0;
            transition: opacity 1.5s ease-in-out;
        }
        .bookshelf {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 50px;
        }
        .book {
            width: 100px;
            height: 150px;
            background: url('book_texture.jpg') no-repeat center;
            background-size: cover;
            cursor: pointer;
            transition: transform 0.3s ease-in-out;
        }
        .book:hover {
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <div class="intro">Welcome to The Hollowed Arcana – A Gateway to Forgotten Knowledge</div>
    
    <div class="pillars-container">
        <div class="pillar" onclick="navigate('home')"><div class="statue"></div></div>
        <div class="pillar" onclick="navigate('about')"><div class="statue"></div></div>
        <div class="pillar" onclick="navigate('policy')"><div class="statue"></div></div>
        <div class="pillar" onclick="enterLibrary()"><div class="statue"></div></div>
    </div>
    
    <div id="library-scene">
        <div class="bookshelf">
            <div class="book" onclick="openBook('history')"></div>
            <div class="book" onclick="openBook('mythology')"></div>
            <div class="book" onclick="openBook('recommendations')"></div>
        </div>
    </div>
    
    <script>
        function navigate(page) {
            alert('Navigating to ' + page);
        }
        function enterLibrary() {
            document.getElementById('library-scene').style.display = 'block';
            setTimeout(() => {
                document.getElementById('library-scene').style.opacity = '1';
            }, 100);
        }
        function openBook(section) {
            alert('Opening ' + section + ' book');
        }
    </script>
</body>
</html>
