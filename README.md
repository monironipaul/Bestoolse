
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Word Counter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
            background-color: #f9f9f9;
        }
        textarea {
            width: 100%;
            height: 150px;
            font-size: 16px;
            padding: 10px;
        }
        .count-box {
            margin-top: 10px;
            font-size: 18px;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <h1>Word Counter</h1>
    <textarea id="textInput" placeholder="Type or paste your text here..."></textarea>
    <div class="count-box">
        Words: <span id="wordCount">0</span> | Characters: <span id="charCount">0</span>
    </div>

    <script>
        const textInput = document.getElementById('textInput');
        const wordCount = document.getElementById('wordCount');
        const charCount = document.getElementById('charCount');

        textInput.addEventListener('input', () => {
            const text = textInput.value.trim();
            const words = text === "" ? 0 : text.split(/\s+/).length;
            const chars = text.length;

            wordCount.textContent = words;
            charCount.textContent = chars;
        });
    </script>

</body>
</html>
