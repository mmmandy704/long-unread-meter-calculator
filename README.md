<!DOCTYPE html>
<html>
<head>
    <title>Long Unread Meter Calculator</title>
    <style>
        body {
            font-family: Arial;
            text-align: center;
            padding: 40px;
        }
        input {
            padding: 10px;
            font-size: 18px;
            margin: 10px;
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            background-color: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
        }
        .result {
            margin-top: 20px;
            font-size: 20px;
        }
    </style>
</head>

<body>

<h1>Long Unread Meter Fine Calculator</h1>

<p>Enter number of long unread meters:</p>

<input type="number" id="meters" placeholder="e.g. 15160">

<br>

<button onclick="calculate()">Calculate</button>

<div class="result" id="output"></div>

<script>
function calculate() {
    let meters = document.getElementById("meters").value;

    let year1 = meters * 40;
    let additional = meters * 80;
    let total = year1 + additional;

    document.getElementById("output").innerHTML =
        "Year 1 Fine: £" + year1.toLocaleString() + "<br>" +
        "Additional Fine (18–24 months): £" + additional.toLocaleString() + "<br>" +
        "<strong>Total Exposure: £" + total.toLocaleString() + "</strong>";
}
</script>

</body>
</html>
