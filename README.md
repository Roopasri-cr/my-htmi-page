<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deep Fake & AI Morphing Detector</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            background: url('./n.png') no-repeat center center fixed;
            background-size: cover;
            color: #333;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
            backdrop-filter: brightness(0.8);
        }

        header {
            background: rgba(37, 117, 252, 0.8);
            color: white;
            padding: 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { text-shadow: 0 0 10px #fff, 0 0 20px #2575fc, 0 0 30px #6a11cb; }
            to { text-shadow: 0 0 20px #fff, 0 0 30px #2575fc, 0 0 40px #6a11cb; }
        }

        h1 {
            font-size: 2.5em;
            font-weight: bold;
            position: relative;
            z-index: 2;
        }

        main {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center; 
            position: relative;
        }

        .container {
            background: rgba(255, 255, 255, 0.9);
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.2);
            max-width: 400px;
            width: 100%;
            text-align: center;
            position: relative;
        }

        .input-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            font-size: 1.2em;
            margin-bottom: 10px;
            color: #6a11cb;
        }

        input[type="file"] {
            padding: 10px;
            border-radius: 5px;
            border: 2px solid #2575fc;
            width: 100%;
            font-size: 1em;
            cursor: pointer;
            background-color: #f1f1f1;
            transition: background-color 0.3s, box-shadow 0.3s;
        }

        input[type="file"]:hover {
            background-color: #e1e1e1;
            box-shadow: 0 0 10px rgba(37, 117, 252, 0.5);
        }

        button {
            background: #6a11cb;
            background: linear-gradient(to right, #2575fc, #6a11cb);
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 25px;
            font-size: 1.2em;
            cursor: pointer;
            transition: background 0.3s;
            animation: pulse 1.5s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        button:hover {
            background: #2575fc;
        }

        footer {
            background: #333;
            color: #ffffffaa;
            text-align: center;
            padding: 10px;
            font-size: 0.9em;
        }

    </style>
</head>
<body>
    <header>
        <h1>Deep Fake & AI Morphing Detector</h1>
    </header>
    <main>
        <div class="container">
            <form id="upload-form">
                <div class="input-group">
                    <label for="photo">Upload Photo</label>
                    <input type="file" id="photo" accept="image/*">
                </div>
                <div class="input-group">
                    <label for="video">Upload Video</label>
                    <input type="file" id="video" accept="video/*">
                </div>
                <button type="submit">Analyze</button>
            </form>
        </div>
    </main>
    <footer>
        <p>&copy; 2024 Deep Fake Detector. All Rights Reserved.</p>
    </footer>
</body>
</html>
