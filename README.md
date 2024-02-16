<!DOCTYPE html>
<html lang="en">
<head>
  <title>My Love Website</title>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body {
      font-family: Arial, Helvetica, sans-serif;
      background-color: pink;
      text-align: center;
    }

    h1 {
      font-size: 40px;
      color: white;
    }

    p {
      font-size: 20px;
      color: white;
    }

    #timer {
      font-size: 30px;
      color: white;
    }
  </style>
</head>
<body>
  <h1>My Baby's Timer </h1>
  <p>This website is dedicated to my pretty girl, who's made me the luckiest man since September 17th, 2022.</p>
  <p>We've been together for:</p>
  <p id="timer"></p>
  <script>
    // Create a variable that stores the date when you started dating
    var startDate = new Date(2022, 8, 17); // Note: month is zero-based

    // Create a function that updates the timer
    function updateTimer() {
      // Get the current date and time
      var currentDate = new Date();

      // Calculate the difference between the current date and the start date
      var difference = currentDate - startDate;

      // Convert the difference to years, months, days, hours, minutes, and seconds
      var years = Math.floor(difference / 1000 / 60 / 60 / 24 / 365);
      difference -= years * 1000 * 60 * 60 * 24 * 365;
      var months = Math.floor(difference / 1000 / 60 / 60 / 24 / 30);
      difference -= months * 1000 * 60 * 60 * 24 * 30;
      var days = Math.floor(difference / 1000 / 60 / 60 / 24);
      difference -= days * 1000 * 60 * 60 * 24;
      var hours = Math.floor(difference / 1000 / 60 / 60);
      difference -= hours * 1000 * 60 * 60;
      var minutes = Math.floor(difference / 1000 / 60);
      difference -= minutes * 1000 * 60;
      var seconds = Math.floor(difference / 1000);

      // Format the timer with leading zeros
      years = years.toString().padStart(2, "0");
      months = months.toString().padStart(2, "0");
      days = days.toString().padStart(2, "0");
      hours = hours.toString().padStart(2, "0");
      minutes = minutes.toString().padStart(2, "0");
      seconds = seconds.toString().padStart(2, "0");

      // Display the timer on the web page
      document.getElementById("timer").innerHTML = `${years} years, ${months} months, ${days} days, ${hours} hours, ${minutes} minutes, ${seconds} seconds`;
    }

    // Call the updateTimer function every second
    setInterval(updateTimer, 1000);
  </script>

  <!-- Add a paragraph element with the text "until eternity" -->
  <p>until eternity</p>

  <!-- Add an image element with the gif source and an alternative text -->
  <iframe src="https://giphy.com/embed/9QI3sUKDDj3eo" width="480" height="416" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/cat-love-kitten-9QI3sUKDDj3eo">via GIPHY</a></p>

</body>
</html>
