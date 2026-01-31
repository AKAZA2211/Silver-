# Silver-<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>College Competition 2026</title>
  <style>
    /* Google Fonts */
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

    * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Roboto', sans-serif; }

    body { background-color: #f0f4f8; color: #333; }

    /* Hero Section */
    header {
      background: linear-gradient(135deg, #4e73df, #1cc88a);
      color: white;
      text-align: center;
      padding: 100px 20px;
    }
    header h1 { font-size: 3em; margin-bottom: 20px; }
    header p { font-size: 1.2em; margin-bottom: 30px; }
    header .cta { background: #fff; color: #4e73df; padding: 15px 30px; border-radius: 30px; text-decoration: none; font-weight: bold; transition: 0.3s; }
    header .cta:hover { background: #e2e6ea; }

    /* Countdown */
    #countdown { font-size: 1.5em; margin-top: 20px; }

    /* Section Styling */
    section {
      max-width: 900px;
      margin: 80px auto;
      padding: 0 20px;
    }
    section h2 { font-size: 2em; margin-bottom: 20px; color: #4e73df; }
    section p { font-size: 1.1em; line-height: 1.6; margin-bottom: 20px; }

    /* Rules */
    ul { margin-left: 20px; list-style-type: disc; }

    /* Form */
    form {
      display: flex;
      flex-direction: column;
      gap: 15px;
      background: #fff;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.1);
    }
    input, textarea, button {
      padding: 12px;
      border-radius: 6px;
      border: 1px solid #ccc;
      font-size: 1em;
      width: 100%;
    }
    button {
      background: #4e73df;
      color: #fff;
      border: none;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover { background: #3753b3; }

    /* Footer */
    footer {
      background: #333;
      color: #fff;
      text-align: center;
      padding: 30px 20px;
      margin-top: 50px;
    }

    @media (max-width: 600px) {
      header h1 { font-size: 2.2em; }
      section h2 { font-size: 1.6em; }
    }
  </style>
</head>
<body>

  <!-- Hero Section -->
  <header>
    <h1>Ultimate College Challenge 2026</h1>
    <p>Show your talent, creativity, and skills. Exciting prizes await!</p>
    <a href="#register" class="cta">Register Now</a>
    <div id="countdown"></div>
  </header>

  <!-- About Section -->
  <section>
    <h2>About the Competition</h2>
    <p>Join us for an exciting competition organized by [Your College Name]. Open to all students who want to showcase their talent and win amazing prizes. Don’t miss your chance to be the champion!</p>
  </section>

  <!-- Rules Section -->
  <section>
    <h2>Rules & Guidelines</h2>
    <ul>
      <li>Open for all college students.</li>
      <li>Individual or team participation allowed (max 4 per team).</li>
      <li>Registration closes on <strong>15th Feb 2026</strong>.</li>
      <li>Follow the competition guidelines strictly.</li>
    </ul>
  </section>

  <!-- Registration Section -->
  <section id="register">
    <h2>Register Now</h2>
    <form action="https://docs.google.com/forms/d/e/your-form-link/formResponse" method="POST" target="_blank">
      <input type="text" name="entry.123456" placeholder="Full Name" required>
      <input type="email" name="entry.654321" placeholder="Email" required>
      <input type="text" name="entry.111222" placeholder="College Name" required>
      <textarea name="entry.333444" placeholder="Team Members (if any)" rows="3"></textarea>
      <button type="submit">Submit Registration</button>
    </form>
  </section>

  <!-- Contact Section -->
  <section>
    <h2>Contact Us</h2>
    <p>Email: competitions@yourcollege.edu</p>
    <p>WhatsApp: +91 XXXXX XXXXX</p>
  </section>

  <!-- Footer -->
  <footer>
    &copy; 2026 [Your College Name]. All rights reserved.
  </footer>

  <!-- Countdown Script -->
  <script>
    const eventDate = new Date("Feb 20, 2026 10:00:00").getTime();
    const countdownEl = document.getElementById("countdown");

    const countdown = setInterval(() => {
      const now = new Date().getTime();
      const distance = eventDate - now;

      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);

      countdownEl.innerHTML = `Starts in: ${days}d ${hours}h ${minutes}m ${seconds}s`;

      if(distance < 0) {
        clearInterval(countdown);
        countdownEl.innerHTML = "The Competition has started!";
      }
    }, 1000);
  </script>

</body>
</html>