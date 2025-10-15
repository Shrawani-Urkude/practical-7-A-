# practical-7-A-
<!DOCTYPE html>
<html>
<head>
  <title>Arithmetic Operations</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f9;
      text-align: center;
      margin-top: 60px;
    }
    h2 {
      color: #333;
    }
    input {
      padding: 8px;
      margin: 5px;
      width: 100px;
      font-size: 16px;
    }
    button {
      padding: 10px 15px;
      margin: 5px;
      font-size: 16px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
    #result {
      margin-top: 20px;
      font-size: 18px;
      color: #333;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <h2>Arithmetic Operations</h2>

  <input type="number" id="num1" placeholder="Enter number 1">
  <input type="number" id="num2" placeholder="Enter number 2">
  <br>

  <button onclick="add()">Add</button>
  <button onclick="subtract()">Subtract</button>
  <button onclick="multiply()">Multiply</button>
  <button onclick="divide()">Divide</button>

  <div id="result"></div>

  <script>
    function getValues() {
      const num1 = parseFloat(document.getElementById("num1").value);
      const num2 = parseFloat(document.getElementById("num2").value);
      return { num1, num2 };
    }

    function add() {
      const { num1, num2 } = getValues();
      document.getElementById("result").innerText = `Result: ${num1 + num2}`;
    }

    function subtract() {
      const { num1, num2 } = getValues();
      document.getElementById("result").innerText = `Result: ${num1 - num2}`;
    }

    function multiply() {
      const { num1, num2 } = getValues();
      document.getElementById("result").innerText = `Result: ${num1 * num2}`;
    }

    function divide() {
      const { num1, num2 } = getValues();
      if (num2 === 0) {
        document.getElementById("result").innerText = "Error: Division by zero!";
      } else {
        document.getElementById("result").innerText = `Result: ${num1 / num2}`;
      }
    }
  </script>

</body>
</html>
