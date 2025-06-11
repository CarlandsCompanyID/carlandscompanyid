<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Jam Seluruh Indonesia</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f0f0f0;
      padding: 40px;
    }
    h1 {
      margin-bottom: 40px;
    }
    .clock {
      background: #ffffff;
      padding: 20px;
      margin: 10px auto;
      width: 300px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 10px;
      font-size: 1.8em;
    }
  </style>
</head>
<body>
  <h1>Jam Digital Seluruh Indonesia</h1>

  <div class="clock" id="wib">WIB (Jakarta): </div>
  <div class="clock" id="wita">WITA (Makassar): </div>
  <div class="clock" id="wit">WIT (Jayapura): </div>

  <script>
    function updateIndonesianClocks() {
      const now = new Date();
      const options = {
        hour: '2-digit',
        minute: '2-digit',
        second: '2-digit',
        hour12: false
      };

      document.getElementById("wib").textContent = 
        "WIB (Jakarta): " + now.toLocaleTimeString("id-ID", { ...options, timeZone: "Asia/Jakarta" });

      document.getElementById("wita").textContent = 
        "WITA (Makassar): " + now.toLocaleTimeString("id-ID", { ...options, timeZone: "Asia/Makassar" });

      document.getElementById("wit").textContent = 
        "WIT (Jayapura): " + now.toLocaleTimeString("id-ID", { ...options, timeZone: "Asia/Jayapura" });
    }

    setInterval(updateIndonesianClocks, 1000);
    updateIndonesianClocks();
  </script>
</body>
</html>
