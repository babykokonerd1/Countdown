<!DOCTYPE html>
<html>
<head>
<title>Countdown</title>

<style>
body {
  background: black;
  margin: 0;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

h1 {
  color: white;
  font-family: Impact, sans-serif;
  font-size: 80px;
}
</style>

</head>

<body>

<h1 id="countdown"></h1>

<script>
const target = new Date("July 4, 2026 00:00:00").getTime();

function updateCountdown() {
  const now = new Date().getTime();
  const distance = target - now;

  const days = Math.floor(distance / (1000 * 60 * 60 * 24));
  const hours = Math.floor((distance / (1000 * 60 * 60)) % 24);
  const seconds = Math.floor((distance / 1000) % 60);

  document.getElementById("countdown").innerHTML =
    days + " " + hours + " " + seconds;
}

setInterval(updateCountdown, 1000);
updateCountdown();
</script>

</body>
</html>
