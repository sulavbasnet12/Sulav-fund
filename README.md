<!DOCTYPE html>
<html>
<head>
  <title>Emergency Lunch Fund</title>
  <style>
    body {
      font-family: Arial;
      text-align: center;
      background: #f8f9fa;
      padding: 50px;
    }
    .box {
      background: white;
      padding: 30px;
      border-radius: 15px;
      max-width: 500px;
      margin: auto;
    }
    button {
      padding: 15px;
      font-size: 18px;
      background: green;
      color: white;
      border: none;
      border-radius: 10px;
    }
  </style>
</head>
<body>

<div class="box">
  <h1>🚨 Emergency grocerry Fund 🚨</h1>
  <p>I am currently broke and hungry cause i have no job and doing placement for free in hospital 😭</p>
  <h2>Goal: $500</h2>

  <button onclick="donate()">Donate Now 💸</button>

  <p id="msg"></p>
</div>

<script>
function donate() {
  document.getElementById("msg").innerHTML =
  "Thank you 😂 now send real money cause no money no honey!";
}
</script>

</body>
</html>
