# Virus_prank
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>SECURITY ALERT</title>
<style>
body {
  background: black;
  color: #ff3333;
  font-family: monospace;
  padding: 30px;
}
h1 {
  text-align: center;
  margin-bottom: 30px;
  font-size: 28px;
}
.console {
  font-size: 15px;
  white-space: pre-wrap;
}
.joke {
  display: none;
  color: #00ff00;
  font-size: 22px;
  font-weight: bold;
  margin-top: 50px;
  text-align: center;
}
</style>
<script>
function fakeAttack(lines, delay) {
  let i = 0;
  let element = document.getElementById("console");
  let interval = setInterval(() => {
    if (i < lines.length) {
      element.textContent += lines[i] + "\n";
      i++;
    } else {
      clearInterval(interval);
      document.getElementById("joke").style.display = "block";
    }
  }, delay);
}
window.onload = () => {
  let msgs = [
    "[!] ACCESSING SYSTEM FILES",
    "[!] BYPASSING SECURITY",
    "[!] ENCRYPTING STORAGE",
    "[!] SCANNING PERSONAL DATA",
    "[!] CONNECTING TO REMOTE SERVER",
    "[!] STATUS: CRITICAL",
    "[!] DEVICE COMPROMISED",
  ];
  fakeAttack(msgs, 600);
};
</script>
</head>
<body>
<h1>⚠ SYSTEM SECURITY BREACH ⚠</h1>
<div id="console" class="console"></div>
<div id="joke" class="joke">😂 RELAX — IT'S A PRANK! 😂</div>
</body>
</html>
