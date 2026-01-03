english-learning-app/
│
├── index.html
├── style.css
└── script.js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>English Learning App</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="app">
        <h1>📘 English Learning</h1>

        <div class="card">
            <p id="word">Hello</p>
            <p id="meaning">A greeting</p>
        </div>

        <button onclick="nextWord()">Next</button>
    </div>

    <script src="script.js"></script>
</body>
</html>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #f2f5f9;
}

.app {
    max-width: 400px;
    margin: auto;
    padding: 20px;
    text-align: center;
}

h1 {
    color: #2c3e50;
}

.card {
    background-color: white;
    padding: 30px;
    margin: 30px 0;
    border-radius: 12px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

#word {
    font-size: 28px;
    font-weight: bold;
    color: #2980b9;
}

#meaning {
    font-size: 18px;
    color: #555;
    margin-top: 10px;
}

button {
    padding: 12px 25px;
    font-size: 16px;
    border: none;
    border-radius: 25px;
    background-color: #2980b9;
    color: white;
    cursor: pointer;
}

button:active {
    background-color: #1f6391;
}
const words = [
    { word: "Hello", meaning: "A greeting" },
    { word: "Book", meaning: "Something you read" },
    { word: "Happy", meaning: "Feeling good" },
    { word: "Learn", meaning: "To get knowledge" },
    { word: "Friend", meaning: "Someone you like and trust" }
];

let index = 0;

function nextWord() {
    index++;

    if (index >= words.length) {
        index = 0;
    }

    document.getElementById("word").innerText = words[index].word;
    document.getElementById("meaning").innerText = words[index].meaning;
}
