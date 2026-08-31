<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>MicroJob - ছোট কাজ, সহজ আয়</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      background: #f5f7fb;
      color: #222;
    }

    /* Navbar */
    nav {
      background: #ffffff;
      padding: 15px 7%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 10px rgba(0,0,0,0.08);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .logo {
      font-size: 25px;
      font-weight: bold;
      color: #2563eb;
    }

    nav a {
      text-decoration: none;
      color: #333;
      margin-left: 20px;
      font-weight: 600;
    }

    .login-btn {
      background: #2563eb;
      color: white !important;
      padding: 10px 18px;
      border-radius: 8px;
    }

    /* Hero */
    .hero {
      background: linear-gradient(135deg, #2563eb, #4f46e5);
      color: white;
      text-align: center;
      padding: 80px 20px;
    }

    .hero h1 {
      font-size: 42px;
      margin-bottom: 15px;
    }

    .hero p {
      font-size: 19px;
      margin-bottom: 30px;
    }

    .hero button {
      border: none;
      background: white;
      color: #2563eb;
      padding: 13px 25px;
      border-radius: 8px;
      font-size: 16px;
      font-weight: bold;
      cursor: pointer;
    }

    /* Container */
    .container {
      width: 90%;
      max-width: 1100px;
      margin: 40px auto;
    }

    .section-title {
      text-align: center;
      margin-bottom: 30px;
      font-size: 30px;
    }

    /* Stats */
    .stats {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      margin-bottom: 50px;
    }

    .stat-card {
      background: white;
      padding: 25px;
      text-align: center;
      border-radius: 12px;
      box-shadow: 0 3px 12px rgba(0,0,0,0.08);
    }

    .stat-card h2 {
      color: #2563eb;
      margin-bottom: 8px;
    }

    /* Jobs */
    .jobs {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .job-card {
      background: white;
      padding: 22px;
      border-radius: 12px;
      box-shadow: 0 3px 12px rgba(0,0,0,0.08);
      transition: 0.3s;
    }

    .job-card:hover {
      transform: translateY(-5px);
    }

    .job-card h3 {
      margin-bottom: 12px;
      color: #222;
    }

    .job-card p {
      color: #666;
      line-height: 1.6;
      margin-bottom: 12px;
    }

    .price {
      color: #16a34a;
      font-weight: bold;
      font-size: 18px;
    }

    .job-btn {
      display: block;
      width: 100%;
      border: none;
      background: #2563eb;
      color: white;
      padding: 11px;
      border-radius: 7px;
      margin-top: 15px;
      cursor: pointer;
      font-size: 15px;
    }

    .job-btn:hover {
      background: #1d4ed8;
    }

    /* How it works */
    .steps {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      margin-top: 30px;
    }

    .step {
      background: white;
      padding: 25px;
      text-align: center;
      border-radius: 12px;
    }

    .step-number {
      width: 45px;
      height: 45px;
      line-height: 45px;
      margin: 0 auto 15px;
      border-radius: 50%;
      background: #2563eb;
      color: white;
      font-weight: bold;
    }

    /* Login */
    .login-box {
      background: white;
      width: 90%;
      max-width: 420px;
      margin: 50px auto;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 3px 15px rgba(0,0,0,0.1);
    }

    .login-box h2 {
      text-align: center;
      margin-bottom: 25px;
    }

    .login-box input {
      width: 100%;
      padding: 13px;
      margin-bottom: 15px;
      border: 1px solid #ddd;
      border-radius: 7px;
      font-size: 15px;
    }

    .login-box button {
      width: 100%;
      padding: 13px;
      border: none;
      border-radius: 7px;
      background: #2563eb;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }

    /* Footer */
    footer {
      background: #111827;
      color: white;
      text-align: center;
      padding: 30px 15px;
      margin-top: 60px;
    }

    /* Mobile */
    @media (max-width: 768px) {
      nav {
        padding: 15px 5%;
      }

      nav div:last-child {
        display: none;
      }

      .hero h1 {
        font-size: 32px;
      }

      .stats,
      .jobs,
      .steps {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>

<body>

  <!-- Navbar -->
  <nav>
    <div class="logo">MicroJob</div>

    <div>
      <a href="#home">হোম</a>
      <a href="#jobs">কাজ</a>
      <a href="#how">কিভাবে কাজ করে</a>
      <a href="#login" class="login-btn">Login</a>
    </div>
  </nav>


  <!-- Hero Section -->
  <section class="hero" id="home">
    <h1>ছোট কাজ করুন, সহজে আয় করুন 💰</h1>

    <p>
      MicroJob প্ল্যাটফর্মে ছোট ছোট কাজ করে অনলাইনে আয় করুন।
    </p>

    <button onclick="goToJobs()">
      কাজ দেখুন
    </button>
  </section>


  <!-- Statistics -->
  <div class="container">

    <div class="stats">

      <div class="stat-card">
        <h2>১০০০+</h2>
        <p>সক্রিয় ইউজার</p>
      </div>

      <div class="stat-card">
        <h2>৫০০+</h2>
        <p>উপলব্ধ কাজ</p>
      </div>

      <div class="stat-card">
        <h2>৳৫০,০০০+</h2>
        <p>মোট পেমেন্ট</p>
      </div>

    </div>


    <!-- Jobs -->
    <section id="jobs">

      <h2 class="section-title">
        Available MicroJobs
      </h2>

      <div class="jobs">

        <div class="job-card">
          <h3>Facebook Page Follow</h3>

          <p>
            নির্দিষ্ট Facebook Page Follow করে Screenshot জমা দিন।
          </p>

          <span class="price">৳ ১০</span>

          <button class="job-btn"
            onclick="applyJob('Facebook Page Follow')">
            কাজটি করুন
          </button>
        </div>


        <div class="job-card">
          <h3>YouTube Subscribe</h3>

          <p>
            নির্দিষ্ট YouTube Channel Subscribe করে প্রমাণ জমা দিন।
          </p>

          <span class="price">৳ ১৫</span>

          <button class="job-btn"
            onclick="applyJob('YouTube Subscribe')">
            কাজটি করুন
          </button>
        </div>


        <div class="job-card">
          <h3>Website Visit</h3>

          <p>
            নির্দিষ্ট ওয়েবসাইটে গিয়ে কিছু সময় অবস্থান করুন।
          </p>

          <span class="price">৳ ৫</span>

          <button class="job-btn"
            onclick="applyJob('Website Visit')">
            কাজটি করুন
          </button>
        </div>


        <div class="job-card">
          <h3>App Review</h3>

          <p>
            একটি অ্যাপ ব্যবহার করে আপনার মতামত লিখুন।
          </p>

          <span class="price">৳ ২০</span>

          <button class="job-btn"
            onclick="applyJob('App Review')">
            কাজটি করুন
          </button>
        </div>


        <div class="job-card">
          <h3>Data Entry</h3>

          <p>
            দেওয়া তথ্য নির্দিষ্ট ফর্মে সঠিকভাবে লিখুন।
          </p>

          <span class="price">৳ ২৫</span>

          <button class="job-btn"
            onclick="applyJob('Data Entry')">
            কাজটি করুন
          </button>
        </div>


        <div class="job-card">
          <h3>Image Tagging</h3>

          <p>
            ছবির মধ্যে থাকা নির্দিষ্ট বিষয় চিহ্নিত করুন।
          </p>

          <span class="price">৳ ১২</span>

          <button class="job-btn"
            onclick="applyJob('Image Tagging')">
            কাজটি করুন
          </button>
        </div>

      </div>
    </section>


    <!-- How it works -->
    <section id="how" style="margin-top:70px;">

      <h2 class="section-title">
        কিভাবে কাজ করে?
      </h2>

      <div class="steps">

        <div class="step">
          <div class="step-number">১</div>
          <h3>অ্যাকাউন্ট তৈরি</h3>
          <p>
            প্রথমে একটি ফ্রি অ্যাকাউন্ট তৈরি করুন।
          </p>
        </div>

        <div class="step">
          <div class="step-number">২</div>
          <h3>কাজ সম্পন্ন করুন</h3>
          <p>
            আপনার পছন্দের MicroJob সম্পন্ন করুন।
          </p>
        </div>

        <div class="step">
          <div class="step-number">৩</div>
          <h3>পেমেন্ট নিন</h3>
          <p>
            কাজ যাচাই হওয়ার পর আপনার ব্যালেন্সে টাকা যোগ হবে।
          </p>
        </div>

      </div>

    </section>

  </div>


  <!-- Login -->
  <section id="login">

    <div class="login-box">

      <h2>Login</h2>

      <input
        type="email"
        id="email"
        placeholder="আপনার Email">

      <input
        type="password"
        id="password"
        placeholder="Password">

      <button onclick="login()">
        Login
      </button>

    </div>

  </section>


  <!-- Footer -->
  <footer>

    <h3>MicroJob</h3>

    <p style="margin-top:10px;">
      ছোট কাজ, সহজ আয় 💰
    </p>

    <p style="margin-top:15px;">
      © 2026 MicroJob. All Rights Reserved.
    </p>

  </footer>


  <!-- JavaScript -->
  <script>

    function goToJobs() {
      document.getElementById("jobs")
        .scrollIntoView({
          behavior: "smooth"
        });
    }


    function applyJob(jobName) {

      alert(
        "আপনি '" +
        jobName +
        "' কাজটি নির্বাচন করেছেন।\n\nLogin করার পর কাজটি শুরু করতে পারবেন।"
      );

    }


    function login() {

      const email =
        document.getElementById("email").value;

      const password =
        document.getElementById("password").value;


      if (email === "" || password === "") {

        alert("দয়া করে Email এবং Password দিন।");

        return;
      }


      alert(
        "Demo Login সফল হয়েছে!\n\n" +
        "বাস্তব Login-এর জন্য Backend/Firebase প্রয়োজন।"
      );

    }

  </script>

</body>
</html>
