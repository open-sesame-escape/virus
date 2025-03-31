---
title: 'Login'
date: '2025-03-30T15:23:00-04:00'
---

# CCD Labs Login

<div style="position: relative; display: inline-block; border-style: solid; border-width: 5px; border-color: lightblue; padding: 10px;">
  <!-- Note: scoped attribute allows style within body. -->
  <style type="text/css" scoped>
    .error-message {
      position: absolute;
      top: 50%;
      left: 25%;
      /* transform: translate(-50%, -150%); */
      background-color: red;
      color: white;
      padding: 10px;
      border-radius: 5px;
      display: none;
      /*font-size: 14px;*/
      z-index: 1000; /* Ensures the popup appears above other elements */
    }
    label {
      font-size: x-large;
    }
    input {
      font-size: x-large;
    }
    button {
      font-size: x-large;
    }
  </style>
  <form id="login-form">
    <label for="name">Username:</label>
    <input type="text" id="name" name="name" value="drbeaker" readonly><br/>
    <label for="password">Password:</label>
    <input type="text" id="password" name="password" required><br/>
    <button type="submit">Submit</button>
  </form>
  <div id="error-message" class="error-message">Incorrect Password</div>
</div>

<script>
  document.getElementById('login-form').addEventListener('submit', function(event) {
    event.preventDefault();
    const errorMessage = document.getElementById('error-message');
    // Show error message
    errorMessage.style.display = 'block';
    // Hide error message after 5 seconds
    setTimeout(function() {
      errorMessage.style.display = 'none';
    }, 5000);
  });
</script>

Do not share your password with anyone. It is crucial to keep your passwords
private to protect your personal information and accounts from unauthorized
access. Always keep your passwords secure and use strong, unique ones for each
account. We will never ask you to disclose your password.

[Reset Password](reset)
