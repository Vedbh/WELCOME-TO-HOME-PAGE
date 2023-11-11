<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stylish Calculator</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <style>
   body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: silver;
    margin: 0;
}

.calculator {
    width: 320px;
    text-align: center;
    margin: 0 auto;
    border: 1px solid #333;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
    background-color: #333;
    color: white;
}

.display {
    background-color: #444;
    padding: 10px;
}

#result {
    width: 90%;
    height: 40px;
    border: none;
    background-color: #444;
    color: white;
    font-size: 20px;
}

.buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 5px;
    padding: 10px;
    background-color: #555;
}

.btn {
    width: 100%;
    height: 40px;
    border: none;
    border-radius: 5px;
    background-color: #777;
    color: white;
    font-size: 18px;
    cursor: pointer;
}

.btn:hover {
    background-color: #888;
}
/* Your existing CSS styles... */
h1 {
    font-size: 36px; /* Adjust the font size as desired */
    color: #4a90e2; /* Choose a nice blue color for the heading text */
    padding: 20px; /* Add some padding for spacing */
    /* Use a bright yellow background color */
    border-radius: 10px; /* Add rounded corners for a colorful box effect */
    display: inline-block; /* Make it an inline-block to center-align it properly */
}

footer {
    text-align: center;
    background-color: black;
    color: white;
    padding: 100px;
    font-size: 25px;
    max-width: 800px; /* Adjust the max-width to your preference */
    margin: 0 auto; /* This centers the footer horizontally */
}

    </style>
  <center><h1></h1>
    <div class="calculator">
        <div class="display">
            <input type="text" id="result" value="0" disabled>
        </div>
        <div class="buttons">
            <button class="btn" onclick="clearResult()">C</button>
            <button class="btn" onclick="appendToResult('7')">7</button>
            <button class="btn" onclick="appendToResult('8')">8</button>
            <button class="btn" onclick="appendToResult('9')">9</button>
            <button class="btn" onclick="appendToResult('+')">+</button>
            <button class="btn" onclick="appendToResult('4')">4</button>
            <button class="btn" onclick="appendToResult('5')">5</button>
            <button class="btn" onclick="appendToResult('6')">6</button>
            <button class="btn" onclick="appendToResult('-')">-</button>
            <button class="btn" onclick="appendToResult('1')">1</button>
            <button class="btn" onclick="appendToResult('2')">2</button>
            <button class="btn" onclick="appendToResult('3')">3</button>
            <button class="btn" onclick="appendToResult('')"></button>
            <button class="btn" onclick="appendToResult('0')">0</button>
            <button class="btn" onclick="calculateResult()">=</button>
            <button class="btn" onclick="appendToResult('/')">/</button>
        </div><ul></ul>
    </div><ul></ul>
    <footer>
    𝗪𝗘𝗕 𝗗𝗘𝗩𝗟𝗢𝗣𝗘𝗥 : Ved Bhogayta
</footer>


    <script>
        let result = document.getElementById('result');

function appendToResult(value) {
    if (result.value === '0') {
        result.value = value;
    } else {
        result.value += value;
    }
}

function clearResult() {
    result.value = '0';
}

function calculateResult() {
    try {
        result.value = eval(result.value);
    } catch (error) {
        result.value = 'Please Enter A Vaild Value';
    }
}

    </script>
</body>
</html>
