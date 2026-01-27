# proteaGroup
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Contact Us | Protea Iron and Steel Group</title>

<!-- EmailJS -->
<script src="https://cdn.jsdelivr.net/npm/emailjs-com@3/dist/email.min.js"></script>
<script>
(function(){
  emailjs.init("_jKY2HopxPbzLyIsh");
})();
</script>

<style>
*, *::before, *::after { box-sizing: border-box; }

body {
  margin: 0;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
  background: #f4f6f7;
  color: #111;
}

/* ================= Header ================= */
header {
  position: fixed;
  top: 0;
  width: 100%;
  height: 64px;
  background: rgba(0,0,0,0.85);
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 32px;
  z-index: 1000;
}

.brand {
  display: flex;
  align-items: center;
  gap: 12px;
  font-weight: 600;
}

.brand img { height: 36px; }

nav {
  display: flex;
}

header a {
  color: #fff;
  text-decoration: none;
  margin-left: 24px;
  font-size: 14px;
}

/* ================= Hamburger ================= */
.menu-btn {
  display: none;
  width: 28px;
  height: 20px;
  flex-direction: column;
  justify-content: space-between;
  cursor: pointer;
}

.menu-btn span {
  height: 3px;
  background: #fff;
  border-radius: 2px;
}

/* ================= Mobile Menu ================= */
.mobile-menu {
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.95);
  z-index: 999;
  display: none;
  flex-direction: column;
  padding: 96px 32px;
}

.mobile-menu a {
  color: #fff;
  text-decoration: none;
  font-size: 20px;
  margin-bottom: 24px;
}

.mobile-menu.active {
  display: flex;
}

/* ================= Page ================= */
.page {
  padding: 140px 8vw 80px;
}

.page h1 {
  font-size: 2.6rem;
  margin-bottom: 24px;
}

/* ================= Office ================= */
.office {
  background: #fff;
  border-radius: 16px;
  padding: 36px;
  margin-bottom: 56px;
  box-shadow: 0 20px 50px rgba(0,0,0,0.08);
}

.office h2 { margin-top: 0; }

.badge {
  background: #111;
  color: #fff;
  font-size: 12px;
  padding: 4px 10px;
  border-radius: 999px;
  margin-left: 10px;
}

.office p { line-height: 1.7; }

.office a {
  color: #111;
  text-decoration: underline;
  cursor: pointer;
}

.map {
  margin-top: 24px;
  border-radius: 12px;
  overflow: hidden;
}

/* ================= Modal ================= */
.modal {
  display: none;
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.6);
  z-index: 1100;
  align-items: center;
  justify-content: center;
}

.modal.active { display: flex; }

.modal-content {
  background: #fff;
  max-width: 560px;
  width: 100%;
  border-radius: 16px;
  padding: 36px;
  position: relative;
}

.modal-content label {
  display: block;
  margin-bottom: 6px;
  font-size: 14px;
}

.modal-content input,
.modal-content select,
.modal-content textarea {
  width: 100%;
  padding: 12px;
  margin-bottom: 16px;
  border-radius: 6px;
  border: 1px solid #ccc;
}

.modal-content button {
  background: #f5d300;
  border: none;
  padding: 14px 28px;
  border-radius: 6px;
  cursor: pointer;
}

.close {
  position: absolute;
  top: 16px;
  right: 20px;
  font-size: 22px;
  cursor: pointer;
}

/* ================= Footer ================= */
footer {
  background: linear-gradient(
    to bottom,
    #f2f3f4,
    #e9eaec
  );
  color: #6b7280;
  text-align: center;
  padding: 48px 0;
  font-size: 14px;
  border-top: 1px solid rgba(0,0,0,0.06);
}

/* ================= Responsive ================= */
@media (max-width: 900px) {
  nav { display: none; }
  .menu-btn { display: flex; }
}
</style>
</head>

<body>

<header>
  <div class="brand">
    <img src="images/logo-protea.png" alt="">
    <span>Protea Iron and Steel Group</span>
  </div>

  <nav>
    <a href="index.html">Home</a>
    <a href="about.html">About us</a>
    <a href="operations.html">Operations</a>
    <a href="careers.html">Careers</a>
    <a href="contact.html">Contact us</a>
  </nav>

  <div class="menu-btn" onclick="toggleMenu()">
    <span></span>
    <span></span>
    <span></span>
  </div>
</header>

<!-- Mobile Menu -->
<div class="mobile-menu" id="mobileMenu">
  <a href="index.html" onclick="toggleMenu()">Home</a>
  <a href="about.html" onclick="toggleMenu()">About us</a>
  <a href="operations.html" onclick="toggleMenu()">Operations</a>
  <a href="careers.html" onclick="toggleMenu()">Careers</a>
  <a href="contact.html" onclick="toggleMenu()">Contact us</a>
</div>

<div class="page">
<h1>Global Offices</h1>

<!-- SOUTH AFRICA -->
<div class="office">
<h2>Cape Town, South Africa <span class="badge">Head Office</span></h2>
<p>
<strong>Address:</strong><br>
Protea Iron and Steel Group<br>
2–7 Karee Road<br>
Kraaifontein Industrial<br>
Cape Town 7570<br>
South Africa
</p>
<p>
<strong>Phone:</strong>
<a onclick="openModal()">+1 616 255 9910</a> /
<a onclick="openModal()">+1 929 494 9248</a> /
<a onclick="openModal()">+27 21 418 9000</a><br>
<strong>Email:</strong>
<a onclick="openModal()">proteaironandsteellptgroup@gmail.com</a> /
<a onclick="openModal()">proteaironandsteellptgroup@outlook.com</a>
</p>
<div class="map">
<iframe src="https://maps.google.com/maps?q=2-7%20Karee%20Road%20Kraaifontein%20Cape%20Town&output=embed" width="100%" height="300"></iframe>
</div>
</div>

<!-- Johannesburg -->
<div class="office">
<h2>Johannesburg, South Africa</h2>
<p>
<strong>Address:</strong><br>
15 Atlas Road<br>
Elandsfontein Industrial<br>
Germiston 1406<br>
South Africa
</p>
<p>
<strong>Phone:</strong> <a onclick="openModal()">+27 11 589 4200</a><br>
<strong>Email:</strong>
<a onclick="openModal()">proteaironandsteellptgroup@gmail.com</a> /
<a onclick="openModal()">proteaironandsteellptgroup@outlook.com</a>
</p>
<div class="map">
<iframe src="https://maps.google.com/maps?q=Germiston%201406%20South%20Africa&output=embed" width="100%" height="300"></iframe>
</div>
</div>

<!-- Durban -->
<div class="office">
<h2>Durban, South Africa</h2>
<p>
<strong>Address:</strong><br>
18 Bayhead Road<br>
Bayhead Industrial<br>
Durban 4001<br>
South Africa
</p>
<p>
<strong>Phone:</strong> <a onclick="openModal()">+27 31 301 8000</a><br>
<strong>Email:</strong>
<a onclick="openModal()">proteaironandsteellptgroup@gmail.com</a> /
<a onclick="openModal()">proteaironandsteellptgroup@outlook.com</a>
</p>
<div class="map">
<iframe src="https://maps.google.com/maps?q=Bayhead%20Road%20Durban&output=embed" width="100%" height="300"></iframe>
</div>
</div>

<!-- New York -->
<div class="office">
<h2>New York, United States</h2>
<p>
<strong>Address:</strong><br>
250 Park Avenue, Suite 1900<br>
New York, NY 10177<br>
United States
</p>
<p>
<strong>Phone:</strong> <a onclick="openModal()">+1 929 494 9248</a><br>
<strong>Email:</strong>
<a onclick="openModal()">proteaironandsteellptgroup@gmail.com</a> /
<a onclick="openModal()">proteaironandsteellptgroup@outlook.com</a>
</p>
<div class="map">
<iframe src="https://maps.google.com/maps?q=250%20Park%20Avenue%20New%20York&output=embed" width="100%" height="300"></iframe>
</div>
</div>

<!-- London -->
<div class="office">
<h2>London, United Kingdom</h2>
<p>
<strong>Address:</strong><br>
One Canada Square<br>
Canary Wharf<br>
London E14 5AB<br>
United Kingdom
</p>
<p>
<strong>Phone:</strong> <a onclick="openModal()">+44 20 7798 1700</a><br>
<strong>Email:</strong>
<a onclick="openModal()">proteaironandsteellptgroup@gmail.com</a> /
<a onclick="openModal()">proteaironandsteellptgroup@outlook.com</a>
</p>
<div class="map">
<iframe src="https://maps.google.com/maps?q=One%20Canada%20Square%20London&output=embed" width="100%" height="300"></iframe>
</div>
</div>

<!-- Berlin -->
<div class="office">
<h2>Berlin, Germany</h2>
<p>
<strong>Address:</strong><br>
Friedrichstraße 123<br>
10117 Berlin<br>
Germany
</p>
<p>
<strong>Phone:</strong> <a onclick="openModal()">+49 30 8892 4400</a><br>
<strong>Email:</strong>
<a onclick="openModal()">proteaironandsteellptgroup@gmail.com</a> /
<a onclick="openModal()">proteaironandsteellptgroup@outlook.com</a>
</p>
<div class="map">
<iframe src="https://maps.google.com/maps?q=Friedrichstrasse%20123%20Berlin&output=embed" width="100%" height="300"></iframe>
</div>
</div>

</div>

<footer>Copyright © 2026 Protea Iron and Steel Group Inc. All rights resverved </footer>

<!-- ================= Modal ================= -->
<div class="modal" id="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal()">×</span>

    <form id="enquiryForm">
      <label>Company name</label>
      <input name="company">

      <label>Name</label>
      <input name="name" required>

      <label>Job title / Position</label>
      <input name="job_title">

      <label>Email</label>
      <input type="email" name="email" required>

      <label>Phone</label>
      <input name="phone">

      <label>Location</label>
      <select name="location">
        <option>United States</option>
        <option>United Kingdom</option>
        <option>Germany</option>
        <option>South Africa</option>
        <option>Australia</option>
        <option>Asia</option>
        <option>Middle East</option>
        <option>Other</option>
      </select>

      <label>Relevant operation</label>
      <select name="operation">
        <option>Aluminum</option>
        <option>Steel</option>
        <option>Copper</option>
        <option>Nickel</option>
        <option>Zinc</option>
        <option>Iron Ore</option>
        <option>Logistics & Trading</option>
        <option>Infrastructure Supply</option>
      </select>

      <label>Message</label>
      <textarea name="message" rows="4"></textarea>

      <button type="submit">Submit</button>
    </form>
  </div>
</div>

<script>
function toggleMenu() {
  document.getElementById("mobileMenu").classList.toggle("active");
}

function openModal() {
  document.getElementById("modal").classList.add("active");
}
function closeModal() {
  document.getElementById("modal").classList.remove("active");
}

document.getElementById("enquiryForm").addEventListener("submit", function(e){
  e.preventDefault();
  emailjs.sendForm("service_8lisu6o","template_zw1ffvb",this)
  .then(()=>{
    alert("Thank you for your enquiry. Our team will contact you shortly.");
    this.reset();
    closeModal();
  });
});
</script>

</body>
</html>
