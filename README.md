# digital-watch
<!DOCTYPE html>
<html>
<head>
<title>Digital Clock</title>
<style>
  #clock {
    font-size: 70px;
    text-align: center;
    margin: 50px;
  }
</style>
</head>
<body>

<div id="clock"></div>

<script>
function updateClock() {
  let now = new Date();
  let hours = now.getHours();
  let minutes = now.getMinutes();
  let seconds = now.getSeconds();

  // Add leading zeros if needed
  hours = hours < 10 ? '0' + hours : hours;
  minutes = minutes < 10 ? '0' + minutes : minutes;
  seconds = seconds < 10 ? '0' + seconds : seconds;

  let currentTime = hours + ':' + minutes + ':' + seconds;
  document.getElementById('clock').innerHTML = currentTime;
}

// Update the clock every second
setInterval(updateClock, 1000);

// Initial call to display the time immediately
updateClock();
</script>

</body>
</html>
