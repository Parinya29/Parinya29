<!DOCTYPE html>
<html>
<head>
  <base target="_top">
  <style>
    body {
      font-family: Arial, sans-serif;
    }
    .container {
      text-align: center;
      margin-top: 20%;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Login Page</h2>
    <form id="loginForm">
      <input type="text" id="username" placeholder="Username" required><br>
      <input type="password" id="password" placeholder="Password" required><br>
      <button type="submit">Login</button>
    </form>
  </div>

  <script>
    document.getElementById("loginForm").addEventListener("submit", function(event) {
      event.preventDefault();
      var username = document.getElementById("username").value;
      var password = document.getElementById("password").value;

      // ส่งข้อมูลไปตรวจสอบหรือประมวลผล
      google.script.run.loginUser(username, password);
    });
  </script>
</body>
</html>

