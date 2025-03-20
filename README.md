<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Modern Minimalist Page</title>
  <style>
    /* Reset styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body, html {
      height: 100%;
      width: 100%;
      font-family: 'Arial', sans-serif;
      overflow: hidden;
    }

    /* Gray-to-black gradient background with stars */
    body {
      background: linear-gradient(180deg, #212121, #000);  /* Updated gray color */
      background-size: 100% 100%;
      color: white;
      position: relative;
      height: 100%;
      overflow: hidden;
    }

    /* Adding the starry background effect */
    .stars {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url('https://www.transparenttextures.com/patterns/stardust.png') repeat;
      z-index: 1;
      pointer-events: none;
      opacity: 0.3;
    }

    /* Centered GUI with darker color and rounded edges */
    .gui {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background-color: #1c1c1c;  /* Darker gray/black color */
      padding: 40px;  /* Increased padding for more length */
      border-radius: 20px;  /* Rounded edges */
      width: 80%;
      max-width: 700px;  /* Increased max-width */
      text-align: center;
      box-shadow: 0 4px 25px rgba(0, 0, 0, 0.7);  /* Deeper shadow for contrast */
      z-index: 2;
    }

    /* Optional text styling for the GUI */
    .gui h1 {
      font-size: 2.5rem;  /* Slightly larger heading */
      color: #fff;
      margin-bottom: 20px;
    }

    .gui p {
      font-size: 1.2rem;  /* Slightly larger text for better readability */
      color: #ccc;
    }

    /* Button Styling for 'Open More Options' */
    .btn {
      background-color: #333;  /* Darker gray for first button */
      color: white;
      border: none;
      padding: 15px 30px;
      font-size: 1rem;
      border-radius: 10px;
      cursor: pointer;
      margin-top: 20px;
      transition: background-color 0.3s ease, transform 0.3s ease;
    }

    .btn:hover {
      background-color: #444;  /* Slightly lighter gray */
      transform: scale(1.05);  /* Slight scaling effect on hover */
    }

    /* The Popup Modal */
    .modal {
      display: none; /* Hidden by default */
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.7);
      z-index: 3;
      justify-content: center;
      align-items: center;
      opacity: 0;  /* Start with invisible modal */
      transition: opacity 0.5s ease;  /* Smooth transition for opacity */
    }

    .modal.show {
      display: flex;  /* Make modal visible */
      opacity: 1;  /* Fade in */
    }

    .modal-content {
      background-color: #333;
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      max-width: 500px;
      width: 80%;
      box-shadow: 0 4px 25px rgba(0, 0, 0, 0.7);
    }

    .modal-content h2 {
      font-size: 2rem;
      color: white;
      margin-bottom: 20px;
    }

    /* Gray Buttons for Modal */
    .modal-content .modal-btn {
      background-color: #333;  /* Same gray as main button */
      color: white;
      padding: 15px 30px;
      border: none;
      border-radius: 10px;
      font-size: 1.2rem;
      cursor: pointer;
      margin: 10px;
      transition: background-color 0.3s ease, transform 0.3s ease;
    }

    .modal-content .modal-btn:hover {
      background-color: #444;  /* Slightly lighter gray on hover */
      transform: scale(1.05);  /* Slight scaling effect on hover */
    }
  </style>
</head>
<body>

  <!-- Background stars -->
  <div class="stars"></div>

  <!-- Centered GUI -->
  <div class="gui">
    <h1>Hello There and welcome.</h1>
    <p>To VoodooGens.</p>
    <button class="btn" id="openModalBtn">Open More Options</button> <!-- Button to open modal -->
  </div>

  <!-- The Modal -->
  <div class="modal" id="myModal">
    <div class="modal-content">
      <h2>Choose an Option</h2>
      <button class="modal-btn" onclick="window.open('https://discord.gg/ygKVYwd6Fg', '_blank');">Join Our Discord</button>
      <button class="modal-btn" onclick="window.open('https://minefort.com', '_blank');">Go to MineFort</button>
    </div>
  </div>

  <script>
    // Get the modal and button
    const modal = document.getElementById("myModal");
    const openModalBtn = document.getElementById("openModalBtn");

    // Function to open the modal
    openModalBtn.onclick = function() {
      modal.classList.add("show");
    }

    // Close the modal when clicked outside
    window.onclick = function(event) {
      if (event.target === modal) {
        modal.classList.remove("show");
      }
    }
  </script>

</body>
</html>
