 <!-- Assigment 1
Smart Profile & Birth Year Calculator -->
<!-- 
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Birth Year Calculator</title>

    <style>

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f0f2f5;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .container {
            background-color: white;
            width: 90%;
            max-width: 450px;
            padding: 35px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        h1 {
            color: #2457a6;
            font-size: 25px;
            margin-bottom: 15px;
        }

        p {
            color: #666;
            font-size: 15px;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        button {
            background-color: #2457a6;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 6px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background-color: #173d78;
        }

        #result {
            margin-top: 20px;
            color: #2457a6;
            font-weight: bold;
            line-height: 1.8;
        }

    </style>

</head>

<body>

    <div class="container">

        <h1>Birth Year Calculator</h1>

        <p>
            Welcome Hasnain! Enter your information
            and calculate your birth year.
        </p>

        <button onclick="calculateBirthYear()">
            Calculate Birth Year
        </button>

        <div id="result"></div>

    </div>


    <script>

        function calculateBirthYear() {

            var name = prompt("Enter your name:", "Hasnain");

            if (name === null || name.trim() === "") {
                alert("Please enter your name.");
                return;
            }

            var age = Number(prompt("Enter your current age:", "17"));

            if (!Number.isInteger(age) || age < 0) {
                alert("Please enter a valid age.");
                return;
            }

            var currentYear = Number(prompt("Enter current year:", "2026"));

            if (!Number.isInteger(currentYear) || currentYear <= 0) {
                alert("Please enter a valid year.");
                return;
            }

            var birthYear = currentYear - age;

            document.getElementById("result").innerHTML =
                "Hello " + name + "!<br>" +
                "Your Age is " + age + "<br>" +
                "Your Birth Year is " + birthYear + "!";

            alert("Hello " + name +
            ", your birth year is " + birthYear + "!");

            console.log("Hello " + name +
            ", your birth year is " + birthYear + "!");

        }

    </script>

</body>

</html> -->

    <!-- Assigment 2
  Smart Supermarket Bill Splitter
  
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Supermarket Bill Splitter</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .container {
            background-color: white;
            width: 90%;
            max-width: 450px;
            padding: 30px;
            border-radius: 10px;
            text-align: center;
        }

        h1 {
            margin-bottom: 15px;
            color: #333;
        }

        p {
            margin-bottom: 20px;
            color: #666;
        }

        button {
            background-color: green;
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: darkgreen;
        }

        #result {
            margin-top: 20px;
            line-height: 2;
            font-weight: bold;
        }
    </style>
</head>

<body>

    <div class="container">

        <h1>Supermarket Bill Splitter</h1>

        <p>Calculate your total bill and split it among family members.</p>

        <button onclick="billSplitter()">Calculate Bill</button>

        <div id="result"></div>

    </div>

    <script>

        function billSplitter() {

            var item1 = Number(prompt("Enter price of Item 1:"));

            var item2 = Number(prompt("Enter price of Item 2:"));

            var item3 = Number(prompt("Enter price of Item 3:"));

            var totalBill = item1 + item2 + item3;

            var members = Number(prompt("Enter total family members:"));

            var share = totalBill / members;

            document.getElementById("result").innerHTML =
                "Total Bill: Rs. " + totalBill + "<br>" +
                "Family Members: " + members + "<br>" +
                "Each Person's Share: Rs. " + share;

            alert("Total Bill: Rs. " + totalBill +
                  "\nEach Person's Share: Rs. " + share);

        }

    </script>

</body>
</html> -->
   <!-- Assigment 3
   Interactive CLI Calculator
   
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Calculator</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .container {
            background-color: white;
            width: 90%;
            max-width: 450px;
            padding: 30px;
            border-radius: 10px;
            text-align: center;
        }

        h1 {
            margin-bottom: 15px;
            color: #333;
        }

        p {
            margin-bottom: 20px;
            color: #666;
        }

        button {
            background-color: green;
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: darkgreen;
        }

        #result {
            margin-top: 20px;
            line-height: 2;
            font-weight: bold;
        }
    </style>
</head>

<body>

    <div class="container">

        <h1>Interactive Calculator</h1>

        <p>Enter two numbers and choose an operator.</p>

        <button onclick="calculator()">Start Calculator</button>

        <div id="result"></div>

    </div>

    <script>

        function calculator() {

            var num1 = Number(prompt("Enter first number:"));

            var num2 = Number(prompt("Enter second number:"));

            var operator = prompt("Enter operator (+, -, *, /):");

            var result;

            if (operator === "+") {
                result = num1 + num2;
            }

            else if (operator === "-") {
                result = num1 - num2;
            }

            else if (operator === "*") {
                result = num1 * num2;
            }

            else if (operator === "/") {
                result = num1 / num2;
            }

            else {
                alert("Invalid operator!");
                return;
            }

            document.getElementById("result").innerHTML =
                "First Number: " + num1 + "<br>" +
                "Second Number: " + num2 + "<br>" +
                "Operator: " + operator + "<br>" +
                "Result: " + result;

            alert("Your Result is: " + result);

        }

    </script>

</body>
</html> -->
