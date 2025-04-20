<!DOCTYPE html>
<html>
<head>
  <title>API Dashboard</title>
</head>
<body>
  <h2>API Status Data</h2>
  <pre id="output">Loading...</pre>

  <script>
    fetch("https://yourapi.azurewebsites.net/api/status")
      .then(res => res.json())
      .then(data => {
        document.getElementById("output").textContent = JSON.stringify(data, null, 2);
      })
      .catch(error => {
        document.getElementById("output").textContent = "Error: " + error;
      });
  </script>
</body>
</html>
