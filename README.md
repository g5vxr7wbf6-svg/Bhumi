# Bhumi
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>For My Favorite Person 💖</title>
  <style>
    body {
      font-family: 'Georgia', serif;
      background: linear-gradient(#fdeff9, #ecf2ff);
      text-align: center;
      padding: 40px;
      color: #5a3d5c;
    }
    .card {
      background: white;
      border-radius: 20px;
      padding: 30px;
      max-width: 500px;
      margin: auto;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    }
    h1 {
      font-size: 28px;
    }
    button {
      background: #f7c1dc;
      border: none;
      border-radius: 25px;
      padding: 12px 25px;
      margin: 10px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #f4a9cc;
    }
    .hidden {
      display: none;
    }
    .gift {
      margin: 15px 0;
      padding: 15px;
      background: #fff3f8;
      border-radius: 15px;
      cursor: pointer;
    }
  </style>
</head>
<body>

<div class="card" id="question">
  <h1>Hey love 💕</h1>
  <p>In my little fairytale world…</p>
  <h2>Do you love me? 🥺</h2>
  <button onclick="yesClicked()">Yes 💖</button>
  <button onclick="noClicked()">No 🙈</button>
</div>

<div class="card hidden" id="gifts">
  <h1>You said YES 😭💘</h1>
  <p>Pick one gift, my love ✨</p>

  <div class="gift" onclick="showMessage('tour')">
    🌍 Foreign Tour
  </div>
  <div class="gift" onclick="showMessage('thanks')">
    💌 Thank You Note
  </div>
  <div class="gift" onclick="showMessage('sorry')">
    🧸 Sorry Message
  </div>

  <p id="message"></p>
</div>

<script>
  function yesClicked() {
    document.getElementById("question").classList.add("hidden");
    document.getElementById("gifts").classList.remove("hidden");
  }

  function noClicked() {
    alert("Wrong answer 😌💔 Try again, pretty please?");
  }

  function showMessage(type) {
    let msg = "";
    if (type === "tour") {
      msg = "🌍 One day, I want to hold your hand in a new country, make memories, take cute photos, and fall in love with you all over again.";
    }
    if (type === "thanks") {
      msg = "💌 Thank you for choosing me, loving me, and being my safe place. You mean more to me than words can ever say.";
    }
    if (type === "sorry") {
      msg = "🧸 I’m sorry for every moment I made you sad. I’m still learning, but my heart is always trying to be better for you.";
    }
    document.getElementById("message").innerText = msg;
  }
</script>

</body>
</html>
