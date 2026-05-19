<!DOCTYPE html>
<html lang="en">

<head>

  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Campus Competition Hub</title>

  <style>

    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:Arial, sans-serif;
    }

    body{
      background:#f4f6f9;
    }

    /* HEADER */

    header{
      background:#1e3a8a;
      color:white;
      text-align:center;
      padding:20px;
    }

    header h1{
      margin-bottom:10px;
    }

    /* NAVBAR */

    nav{
      background:#2563eb;
      padding:15px;
      text-align:center;
      position:sticky;
      top:0;
    }

    nav a{
      color:white;
      text-decoration:none;
      margin:15px;
      font-weight:bold;
    }

    nav a:hover{
      color:yellow;
    }

    /* HERO */

    .hero{
      background:white;
      text-align:center;
      padding:70px 20px;
    }

    .hero h1{
      color:#1e3a8a;
      font-size:42px;
      margin-bottom:20px;
    }

    .hero p{
      color:#555;
      font-size:18px;
      max-width:800px;
      margin:auto;
      line-height:1.6;
    }

    /* MAIN */

    .container{
      padding:40px;
    }

    h2{
      color:#1e3a8a;
      margin-bottom:20px;
    }

    /* EVENT CARDS */

    .events{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
      gap:20px;
    }

    .card{
      background:white;
      padding:20px;
      border-radius:10px;
      box-shadow:0 0 10px rgba(0,0,0,0.1);
    }

    .card h3{
      color:#2563eb;
      margin-bottom:10px;
    }

    .card p{
      margin-bottom:10px;
      color:#555;
      line-height:1.5;
    }

    /* BUTTON */

    .btn{
      background:#2563eb;
      color:white;
      border:none;
      padding:12px 20px;
      border-radius:5px;
      cursor:pointer;
      font-size:16px;
    }

    .btn:hover{
      background:#1e3a8a;
    }

    /* FORM SECTION */

    .form-section{
      background:white;
      margin-top:40px;
      padding:30px;
      border-radius:10px;
      box-shadow:0 0 10px rgba(0,0,0,0.1);
    }

    input, textarea{
      width:100%;
      padding:12px;
      margin-top:10px;
      margin-bottom:20px;
      border:1px solid #ccc;
      border-radius:5px;
      font-size:16px;
    }

    /* FOOTER */

    footer{
      background:#1e3a8a;
      color:white;
      text-align:center;
      padding:15px;
      margin-top:40px;
    }

    /* POPUP */

    #popup{
      display:none;
      position:fixed;
      top:0;
      left:0;
      width:100%;
      height:100%;
      background:rgba(0,0,0,0.6);
      z-index:999;
    }

    .popup-content{
      background:white;
      width:90%;
      max-width:400px;
      padding:30px;
      margin:80px auto;
      border-radius:10px;
    }

  </style>

</head>

<body>

  <!-- HEADER -->

  <header>

    <h1>Campus Competition Hub</h1>

    <p>One Platform for Every Student Opportunity</p>

  </header>

  <!-- NAVBAR -->

  <nav>

    <a href="#home">Home</a>
    <a href="#events">Events</a>
    <a href="#upload">Upload Event</a>
    <a href="#aiagent">AI Agent</a>
    <a href="#contact">Contact</a>

  </nav>

  <!-- HERO SECTION -->

  <section class="hero" id="home">

    <h1>Discover Competitions Easily</h1>

    <p>
      Find hackathons, coding contests, workshops,
      sports and cultural events from different colleges
      in one centralized platform.
    </p>

  </section>

  <!-- EVENTS SECTION -->

  <div class="container" id="events">

    <h2>Upcoming Events</h2>

    <div class="events">

      <!-- EVENT 1 -->

      <div class="card">

        <h3>AI Hackathon 2026</h3>

        <p><strong>College:</strong> XYZ Engineering College</p>

        <p><strong>Date:</strong> 25 May 2026</p>

        <p>
          Build innovative AI solutions and compete with students nationwide.
        </p>

        <button class="btn" onclick="openPopup()">

          Register

        </button>

      </div>

      <!-- EVENT 2 -->

      <div class="card">

        <h3>Web Development Workshop</h3>

        <p><strong>Organizer:</strong> ABC University</p>

        <p><strong>Date:</strong> 30 May 2026</p>

        <p>
          Learn frontend and backend development from industry experts.
        </p>

        <button class="btn" onclick="openPopup()">

          Register

        </button>

      </div>

      <!-- EVENT 3 -->

      <div class="card">

        <h3>National Coding Contest</h3>

        <p><strong>Organizer:</strong> Tech Community</p>

        <p><strong>Date:</strong> 10 June 2026</p>

        <p>
          Showcase your coding skills and win exciting prizes.
        </p>

        <button class="btn" onclick="openPopup()">

          Register

        </button>

      </div>

    </div>

    <!-- UPLOAD EVENT -->

    <div class="form-section" id="upload">

      <h2>Upload New Event</h2>

      <form onsubmit="uploadEvent(event)">

        <label>Event Name</label>

        <input type="text"
        placeholder="Enter event name"
        required>

        <label>College / Organization</label>

        <input type="text"
        placeholder="Enter college name"
        required>

        <label>Date</label>

        <input type="date"
        required>

        <label>Description</label>

        <textarea rows="5"
        placeholder="Enter event details"
        required></textarea>

        <button type="submit" class="btn">

          Upload Event

        </button>

      </form>

    </div>

    <!-- AI AGENT -->

    <div class="form-section" id="aiagent">

      <h2>AI Event Tracking Agent</h2>

      <p>
        Our AI Agent automatically scans college social media pages,
        websites and online posters to identify upcoming competitions,
        hackathons and workshops.
      </p>

      <br>

      <p>
        The AI extracts event names, dates, timings,
        venues and registration links using intelligent
        web scraping and NLP techniques, then updates
        the platform automatically in real-time.
      </p>

      <br>

      <button class="btn" onclick="runAI()">

        Run AI Agent

      </button>

    </div>

    <!-- CONTACT -->

    <div class="form-section" id="contact">

      <h2>Contact</h2>

      <p>Email: campushub@gmail.com</p>

      <p>Phone: +91 9876543210</p>

    </div>

  </div>

  <!-- REGISTRATION POPUP -->

  <div id="popup">

    <div class="popup-content">

      <h2 style="color:#1e3a8a;margin-bottom:20px;">

        Event Registration Form

      </h2>

      <form onsubmit="submitRegistration(event)">

        <input type="text"
        placeholder="Full Name"
        required>

        <input type="email"
        placeholder="Email Address"
        required>

        <input type="text"
        placeholder="College Name"
        required>

        <input type="tel"
        placeholder="Phone Number"
        required>

        <button type="submit" class="btn">

          Submit Registration

        </button>

        <button type="button"
        class="btn"
        style="background:red;margin-top:10px;"
        onclick="closePopup()">

          Close

        </button>

      </form>

    </div>

  </div>

  <!-- FOOTER -->

  <footer>

    <p>
      © 2026 Campus Competition Hub |
      Developed for Hackathon Prototype
    </p>

  </footer>

  <!-- JAVASCRIPT -->

  <script>

    // OPEN REGISTRATION FORM

    function openPopup(){

      document.getElementById("popup").style.display = "block";

    }

    // CLOSE REGISTRATION FORM

    function closePopup(){

      document.getElementById("popup").style.display = "none";

    }

    // REGISTRATION SUCCESS

    function submitRegistration(event){

      event.preventDefault();

      alert("Registration Successful!");

      closePopup();

    }

    // UPLOAD EVENT SUCCESS

    function uploadEvent(event){

      event.preventDefault();

      alert("Event Uploaded Successfully!");

    }

    // AI AGENT

    function runAI(){

      alert("AI Agent scanned college social media pages and updated latest events successfully!");

    }

  </script>

</body>

</html>
