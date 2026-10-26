# digital-clock

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Digital Clock</title>
<style>
body{margin:0;background:#101525;color:#72ffe0;font-family:Arial;display:grid;place-items:center;min-height:100vh;text-align:center}
.card{padding:35px;border:1px solid #315b66;border-radius:20px;background:#192337;box-shadow:0 0 35px #00ffc322}
#clock{font-size:clamp(40px,12vw,75px);font-weight:bold}
p{color:#b4c8db}
</style>
</head>
<body>
<div class="card">
<h1>⌚ Digital Clock</h1>
<div id="clock">00:00:00</div>
<p id="date"></p>
</div>
<script>
function update(){
const now=new Date();
document.getElementById("clock").textContent=
now.toLocaleTimeString("en-IN",{hour12:true});
document.getElementById("date").textContent=
now.toLocaleDateString("en-IN",{weekday:"long",day:"numeric",month:"long",year:"numeric"});
}
update();
setInterval(update,1000);
</script>
</body>
</html>
