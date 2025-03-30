---
title: 'Password Reset'
date: '2025-03-30T16:32:52-04:00'
---

# Password Reset

<div style="position: relative; display: inline-block;">
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
  </style>
  <form id="login-form">
    <p>
      <label for="foods">What are your favorite FOODS?</label>
      <input type="text" id="foods" name="foods" required>
    </p>
    <p>
      <label for="month">What MONTH were you born?</label>
      <input type="text" id="month" name="month" required>
    </p>
    <p>
      <label for="child">What is the name of your CHILD?</label>
      <input type="text" id="child" name="child" required>
    </p>
    <button type="submit">Submit</button>
  </form>
  <div id="error-message" class="error-message">Incorrect Responses</div>
</div>

<script>
  document.getElementById('login-form').addEventListener('submit', function(event) {
    event.preventDefault();
    // Clear any previous error message
    const errorMessage = document.getElementById('error-message');
    errorMessage.style.display = 'none';

    // Get the form fields.
    const foods = document.getElementById('foods').value;
    const month = document.getElementById('month').value;
    const child = document.getElementById('child').value;

    if ((foods.toUpperCase() === 'CANDY') &&
        (month.toUpperCase() === 'MARCH') &&
        (child.toUpperCase() === 'JOHNY')) {
      // Redirect to success page
      window.location.href = '../reset-success';
    } else {
      // Show error message
      errorMessage.style.display = 'block';

      // Hide error message after 5 seconds
      setTimeout(function() {
        errorMessage.style.display = 'none';
      }, 5000);
    }
  });
</script>
