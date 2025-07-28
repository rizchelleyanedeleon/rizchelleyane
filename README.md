<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>RizhelCare by Rizchelleyane De Leon</title>
  <style>
    :root {
      --beige-light: #f9f2ec;
      --beige-bg: #fff0f5;
      --pink-dark: #6e3e4e;
      --pink-medium: #d98ca8;
      --pink-light: #f5e8e4;
      --pink-hover: #a95562;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background: var(--beige-light);
      color: var(--pink-dark);
      line-height: 1.6;
    }

    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: var(--pink-medium);
      color: var(--pink-light);
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;
    }

    header h1 {
      font-size: 1.6rem;
      cursor: pointer;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1.2rem;
    }

    nav button {
      background: transparent;
      border: none;
      color: var(--pink-light);
      font-size: 1rem;
      cursor: pointer;
      padding: 0.4rem 0.7rem;
      border-radius: 4px;
      transition: background 0.3s ease;
    }

    nav button:hover {
      background: rgba(255, 255, 255, 0.2);
    }

    main {
      padding: 100px 2rem 2rem;
      max-width: 1100px;
      margin: auto;
    }

    section {
      background: var(--beige-bg);
      padding: 2rem;
      border-radius: 10px;
      margin-bottom: 2rem;
      box-shadow: 0 2px 10px rgba(110, 62, 78, 0.1);
    }

    .hero {
      background: url('https://images.unsplash.com/photo-1526256262350-7da7584cf5eb?auto=format&fit=crop&w=1350&q=80') center/cover no-repeat;
      color: var(--pink-light);
      text-align: center;
      padding: 4rem 2rem;
      border-radius: 10px;
      margin-bottom: 2rem;
    }

    .hero h2 {
      font-size: 2.5rem;
    }

    .hero p {
      font-size: 1.2rem;
      margin: 1rem 0;
    }

    .hero button {
      background: var(--pink-medium);
      border: none;
      padding: 0.75rem 2rem;
      color: var(--pink-light);
      font-weight: bold;
      border-radius: 25px;
      cursor: pointer;
    }

    h2 {
      color: var(--pink-dark);
      margin-bottom: 1rem;
    }

    input, select, textarea, button {
      width: 100%;
      padding: 0.7rem;
      margin: 0.5rem 0 1rem;
      border-radius: 5px;
      border: 1px solid var(--pink-medium);
    }

    button {
      background: var(--pink-medium);
      color: white;
      font-weight: bold;
      cursor: pointer;
      border: none;
      transition: background 0.3s;
    }

    button:hover {
      background: var(--pink-hover);
    }

    footer {
      background: var(--pink-medium);
      color: white;
      text-align: center;
      padding: 1rem;
    }

    .hospital-card, .doctor-card {
      border: 1px solid var(--pink-medium);
      padding: 1rem;
      border-radius: 8px;
      margin-bottom: 1rem;
    }

    .doctor-card img {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      object-fit: cover;
      float: left;
      margin-right: 1rem;
    }

    .doctor-card h3 {
      margin-top: 0;
    }

    .search-input {
      margin-bottom: 1rem;
      padding: 0.5rem;
      border: 1px solid var(--pink-medium);
      border-radius: 5px;
    }

    #appointment-summary {
      background: var(--pink-light);
      border: 1px solid var(--pink-medium);
      padding: 1rem;
      border-radius: 8px;
      margin-top: 1rem;
      color: var(--pink-dark);
    }

    @media (max-width: 768px) {
      nav ul {
        flex-direction: column;
        gap: 0.5rem;
      }

      .hero h2 {
        font-size: 1.8rem;
      }

      .doctor-card img {
        float: none;
        display: block;
        margin: 0 auto 1rem auto;
      }
    }
  </style>
</head>

<body>

  <header>
    <h1 onclick="scrollToSection('hero')">RizhelCare</h1>
    <nav>
      <ul>
        <li><button onclick="scrollToSection('hospital-list')">Hospitals</button></li>
        <li><button onclick="scrollToSection('doctors')">Doctors</button></li>
        <li><button onclick="scrollToSection('appointments')">Appointments</button></li>
        <li><button onclick="scrollToSection('faq')">FAQ</button></li>
        <li><button onclick="scrollToSection('contact')">Contact</button></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="hero" id="hero">
      <h2>Welcome to RizhelCare</h2>
      <p>A healthcare appointment system designed by Rizchelleyane De Leon.</p>
      <button onclick="scrollToSection('hospital-list')">Get Started</button>
    </section>

    <section id="hospital-list">
      <h2>Hospitals</h2>
      <div class="hospital-list">
        <div class="hospital-card">
          <h3>Sunrise Medical Center</h3>
          <p>Providing exceptional care with a compassionate touch. Located downtown.</p>
          <button type="button" onclick="window.location.href='mailto:contact@sunrisemedical.com?subject=Inquiry'">Contact via Email</button>
        </div>
        <div class="hospital-card">
          <h3>Green Valley Hospital</h3>
          <p>State-of-the-art facilities and experienced specialists in every field.</p>
          <button type="button" onclick="window.location.href='mailto:info@greenvalleyhospital.com?subject=Inquiry'">Contact via Email</button>
        </div>
        <div class="hospital-card">
          <h3>Harmony Health Clinic</h3>
          <p>Community-focused care with a holistic approach to health and wellness.</p>
          <button type="button" onclick="window.location.href='mailto:contact@harmonyhealthclinic.com?subject=Inquiry'">Contact via Email</button>
        </div>
      </div>
    </section>

    <section id="doctors">
      <h2>Doctor Directory</h2>
      <input id="search-doctor" class="search-input" placeholder="Search by name or specialty..." />
      <div class="doctor-list" id="doctor-list">
        <div class="doctor-card" data-name="Dr. Anna Reyes" data-specialty="Dermatology">
          <img src="https://via.placeholder.com/100" alt="Dr. Anna Reyes" />
          <h3>Dr. Anna Reyes</h3>
          <p>Dermatology • ⭐ 4.8</p>
          <button onclick="prefillAppointment('Dr. Anna Reyes')">Book with Dr. Reyes</button>
        </div>
        <div class="doctor-card" data-name="Dr. Mark Santos" data-specialty="Cardiology">
          <img src="https://via.placeholder.com/100" alt="Dr. Mark Santos" />
          <h3>Dr. Mark Santos</h3>
          <p>Cardiology • ⭐ 4.6</p>
          <button onclick="prefillAppointment('Dr. Mark Santos')">Book with Dr. Santos</button>
        </div>
        <div class="doctor-card" data-name="Dr. Lisa Cruz" data-specialty="Pediatrics">
          <img src="https://via.placeholder.com/100" alt="Dr. Lisa Cruz" />
          <h3>Dr. Lisa Cruz</h3>
          <p>Pediatrics • ⭐ 4.9</p>
          <button onclick="prefillAppointment('Dr. Lisa Cruz')">Book with Dr. Cruz</button>
        </div>
      </div>
    </section>

    <section id="appointments">
      <h2>Book an Appointment</h2>
      <form id="appointment-form">
        <label for="patient-name">Full Name</label>
        <input type="text" id="patient-name" required />

        <label for="hospital">Select Hospital</label>
        <select id="hospital" required>
          <option value="" disabled selected>Select a hospital</option>
          <option>Sunrise Medical Center</option>
          <option>Green Valley Hospital</option>
          <option>Harmony Health Clinic</option>
        </select>

        <label for="doctor">Select Doctor</label>
        <select id="doctor" required>
          <option value="" disabled selected>Select a doctor</option>
          <option>Dr. Anna Reyes</option>
          <option>Dr. Mark Santos</option>
          <option>Dr. Lisa Cruz</option>
        </select>

        <label for="date">Date</label>
        <input type="date" id="date" required />

        <label for="time">Time</label>
        <input type="time" id="time" required />

        <button type="submit">Confirm Appointment</button>
      </form>
      <div id="appointment-summary" style="display:none;"></div>
    </section>

    <section id="faq">
      <h2>Frequently Asked Questions</h2>
      <p><strong>Q:</strong> How can I cancel an appointment?<br><strong>A:</strong> Contact the hospital directly.</p>
      <p><strong>Q:</strong> Do I need to register?<br><strong>A:</strong> No registration needed—just fill out the form!</p>
      <p><strong>Q:</strong> Can I reschedule later?<br><strong>A:</strong> Yes, use the hospital contact provided.</p>
    </section>

    <section id="contact">
      <h2>Contact me</h2>
      <p>If you have feedback or feature requests, reach out below.</p>
      <form id="contact-form">
        <label for="dev-name">Your Name</label>
        <input type="text" id="dev-name" required />

        <label for="dev-email">Your Email</label>
        <input type="email" id="dev-email" required />

        <label for="dev-message">Your Message</label>
        <textarea id="dev-message" rows="4" required></textarea>

        <button type="submit">Send Message</button>
      </form>
    </section>
  </main>

  <footer>
    &copy; 2025 RizhelCare | Designed & Developed by Rizchelleyane De Leon | <a href="mailto:rizchelleyane@example.com" style="color: white;">rizchelleyanedeleon@gmail.com</a>
  </footer>

  <script>
    function scrollToSection(id) {
      const section = document.getElementById(id);
      const offset = document.querySelector('header').offsetHeight;
      window.scrollTo({
        top: section.offsetTop - offset,
        behavior: 'smooth'
      });
    }

    // Doctor search/filter
    const searchInput = document.getElementById('search-doctor');
    searchInput.addEventListener('input', function () {
      const filter = this.value.toLowerCase();
      const doctors = document.querySelectorAll('.doctor-card');
      doctors.forEach(doc => {
        const name = doc.getAttribute('data-name').toLowerCase();
        const specialty = doc.getAttribute('data-specialty').toLowerCase();
        if (name.includes(filter) || specialty.includes(filter)) {
          doc.style.display = '';
        } else {
          doc.style.display = 'none';
        }
      });
    });

    // Prefill appointment doctor select and scroll to form
    function prefillAppointment(doctorName) {
      const doctorSelect = document.getElementById('doctor');
      doctorSelect.value = doctorName;
      scrollToSection('appointments');
    }

    // Set minimum date to today for appointment date input
    const today = new Date().toISOString().split('T')[0];
    document.getElementById('date').setAttribute('min', today);

    // Appointment form handler
    document.getElementById('appointment-form').addEventListener('submit', function (e) {
      e.preventDefault();
      const name = document.getElementById('patient-name').value.trim();
      const hospital = document.getElementById('hospital').value;
      const doctor = document.getElementById('doctor').value;
      const date = document.getElementById('date').value;
      const time = document.getElementById('time').value;

      if (!name || !hospital || !doctor || !date || !time) {
        alert('Please fill in all appointment details.');
        return;
      }

      // Validate date/time (cannot book past date/time)
      const appointmentDateTime = new Date(date + 'T' + time);
      if (appointmentDateTime < new Date()) {
        alert('Appointment date and time cannot be in the past.');
        return;
      }

      // Save appointment to localStorage (simple persistence)
      let appointments = JSON.parse(localStorage.getItem('appointments')) || [];
      appointments.push({ name, hospital, doctor, date, time });
      localStorage.setItem('appointments', JSON.stringify(appointments));

      // Show summary and simulate email confirmation alert
      const summaryDiv = document.getElementById('appointment-summary');
      summaryDiv.style.display = 'block';
      summaryDiv.innerHTML = `
        <h3>Appointment Confirmed!</h3>
        <p><strong>Name:</strong> ${name}</p>
        <p><strong>Hospital:</strong> ${hospital}</p>
        <p><strong>Doctor:</strong> ${doctor}</p>
        <p><strong>Date & Time:</strong> ${date} at ${time}</p>
        <p>An email confirmation has been sent to your registered email (simulated).</p>
      `;
      alert(`Appointment confirmed for ${name} with ${doctor} at ${hospital} on ${date} at ${time}.\n\nA confirmation email has been sent.`);

      this.reset();
    });

    // Contact form handler
    document.getElementById('contact-form').addEventListener('submit', function (e) {
      e.preventDefault();
      const devName = document.getElementById('dev-name').value.trim();
      const devEmail = document.getElementById('dev-email').value.trim();
      const devMessage = document.getElementById('dev-message').value.trim();

      if (!devName || !devEmail || !devMessage) {
        alert('Please fill in all contact fields.');
        return;
      }

      alert(`Thanks ${devName}, your message has been sent!`);
      this.reset();
    });
  </script>
</body>
</html>
