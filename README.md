<!DOCTYPE html>
<html>
<head>
	<title>Tax Calculator</title>
</head>
<body>
	<h1>Tax Calculator</h1>
	<form>
		<label for="income">Income:</label>
		<input type="number" id="income" name="income"><br><br>
		
		<label for="tax-rate">Tax Rate:</label>
		<input type="number" id="tax-rate" name="tax-rate"><br><br>
		
		<button type="button" onclick="calculateTax()">Calculate Tax</button>
	</form>
	<br><br>
	<div id="result"></div>
	<script>
		function calculateTax() {
			var income = document.getElementById("income").value;
			var taxRate = document.getElementById("tax-rate").value;
			var tax = income * (taxRate/100);
			document.getElementById("result").innerHTML = "Your tax liability is: $" + tax;
		}
	</script>
</body>
</html>
