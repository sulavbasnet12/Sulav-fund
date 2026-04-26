<!DOCTYPE html>
<html>
<head>
  <title>Emergency Survival Fund</title>
  <style>
    body {
      font-family: Arial;
      background: #f4f6f8;
      text-align: center;
      padding: 40px;
    }
    .box {
      background: white;
      padding: 30px;
      border-radius: 15px;
      max-width: 500px;
      margin: auto;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }
    h1 {
      color: #e63946;
    }
    .progress {
      background: #ddd;
      border-radius: 20px;
      overflow: hidden;
      margin: 20px 0;
    }
    .progress-bar {
      height: 25px;
      width: 2%;
      background: #2a9d8f;
      transition: 0.5s;
    }
    button {
      padding: 15px 25px;
      font-size: 18px;
      background: #2a9d8f;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
    button:hover {
      background: #21867a;
    }
    .donors {
      margin-top: 20px;
      text-align: left;
    }
  </style>
</head>
<body>

<div class="box">
  <h1>🚨 Emergency Survival Fund 🚨</h1>
  
  <p>
    I am currently broke and hungry 😭<br>
    Doing hospital placement for FREE (yes… free labour 💀)<br>
    No job. No income. Just vibes and suffering.
  </p>

  <h3>$<span id="amount">10</span> raised of $500</h3>

  <div class="progress">
    <div class="progress-bar" id="bar"></div>
  </div>

  <button onclick="donate()">Donate Now 💸</button>

  <p id="msg"></p>

  <div class="donors">
    <h4>Top Donors 😂</h4>
    <ul id="list">
      <li>Mom — $5</li>
      <li>Best Friend — $5</li>
    </ul>
  </div>
</div>

<script>
let amount = 10;

function donate() {
  let donation = Math.floor(Math.random() * 20) + 5; // $5–$25
  amount += donation;

  document.getElementById("amount").innerText = amount;

  let percent = (amount / 500) * 100;
  document.getElementById("bar").style.width = percent + "%";

  let names = ["John", "Alex", "Your crush 😏", "Random hero 😂", "Rich uncle", "Future boss"];
  let name = names[Math.floor(Math.random() * names.length)];

  let li = document.createElement("li");
  li.innerText = name + " donated $" + donation;
  document.getElementById("list").appendChild(li);

  document.getElementById("msg").innerHTML =
    "😂 Thank you 😂 now send real money cause no money no honey!";

  if (amount >= 500) {
    document.getElementById("msg").innerHTML =
      "🎉 GOAL REACHED! I CAN FINALLY EAT 🍔😭";
  }
}
</script>

</body>
</html>
