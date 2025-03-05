# handwrttentext
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Text to Handwritten Converter</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Patrick+Hand&display=swap');

        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
            padding: 20px;
        }

        h1 {
            color: #333;
        }

        textarea {
            width: 80%;
            height: 150px;
            font-size: 16px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            resize: none;
        }

        button {
            margin-top: 10px;
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            background-color: #333;
            color: white;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #555;
        }

        .output {
            margin-top: 20px;
            padding: 20px;
            font-size: 24px;
            font-family: 'Patrick Hand', cursive;
            white-space: pre-line;
            border: 1px solid #ddd;
            background-color: white;
            display: inline-block;
            max-width: 80%;
        }
    </style>
</head>
<body>

    <h1>Text to Handwritten Converter</h1>
    <textarea id="userText" placeholder="Enter your text here..."></textarea>
    <br>
    <button onclick="convertText()">Convert to Handwriting</button>
    <br>
    <div id="handwrittenText" class="output"></div>

    <script>
        function convertText() {
            let inputText = document.getElementById("userText").value;
            let outputDiv = document.getElementById("handwrittenText");

            if (inputText.trim() === "") {
                outputDiv.innerHTML = "Please enter some text!";
                return;
            }

            outputDiv.innerText = inputText;
        }
    </script>

</body>
</html>
