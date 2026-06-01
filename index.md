---
layout: home
---

<style>
  /* --- GLOBAL LIGHT/DARK MODE STYLES --- */
  body { transition: background-color 0.3s ease, color 0.3s ease; }
  
  /* Dark Theme Overrides */
  body.dark-theme { background-color: #121212; color: #e0e0e0; }
  body.dark-theme a { color: #64b5f6 !important; }
  body.dark-theme .theme-card { background-color: #1e1e1e !important; border-color: #333 !important; }
  body.dark-theme h1, body.dark-theme h2, body.dark-theme h3, body.dark-theme p, body.dark-theme span, body.dark-theme strong, body.dark-theme li { color: #e0e0e0 !important; }
  body.dark-theme svg { fill: #e0e0e0 !important; }
  body.dark-theme .action-btn { background-color: #64b5f6; color: #121212 !important; }
  body.dark-theme .action-btn:hover { background-color: #90caf9; }
  body.dark-theme .section-header { border-bottom-color: #333; }
  
  /* --- LAYOUT & COMPONENT STYLES --- */
  .theme-toggle-btn { position: fixed; bottom: 20px; right: 20px; background: #333; color: #fff; border: none; border-radius: 50px; padding: 12px 18px; cursor: pointer; z-index: 1000; box-shadow: 0 4px 12px rgba(0,0,0,0.3); transition: background 0.3s; font-weight: bold; font-size: 0.9em; }
  body.dark-theme .theme-toggle-btn { background: #f1f1f1; color: #333; }

  /* Hero Section */
  .hero-container { display: flex; gap: 40px; margin-bottom: 60px; flex-wrap: wrap; }
  .hero-left { flex: 0 0 300px; display: flex; flex-direction: column; }
  .hero-img { width: 300px; height: 400px; object-fit: cover; border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.1); margin-bottom: 15px; }
  .resume-btn { text-align: center; width: 100%; padding: 12px 0; background-color: #0A66C2; color: white !important; text-decoration: none; border-radius: 6px; font-weight: bold; transition: all 0.2s; display: inline-block; box-sizing: border-box; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
  .resume-btn:hover { transform: translateY(-2px); box-shadow: 0 4px 10px rgba(0,0,0,0.2); }
  
  /* By using flex-direction: column and space-between, the text perfectly aligns with the top and bottom of the left column */
  .hero-right { flex: 1; display: flex; flex-direction: column; justify-content: space-between; min-width: 300px; }
  
  .section-header { border-bottom: 2px solid #eaeaea; padding-bottom: 10px; margin-top: 50px; margin-bottom: 25px; font-size: 1.6em; }
  .list-container { padding-left: 20px; line-height: 1.8; margin-bottom: 40px; }
  .list-container li { margin-bottom: 12px; }
  .pub-title { font-weight: bold; }
  /* Center the photo and button on mobile screens */
  @media (max-width: 768px) {
    .hero-left { margin: 0 auto; }
  }
</style>

<!-- THEME TOGGLE SCRIPT & BUTTON -->
<button class="theme-toggle-btn" onclick="toggleTheme()">🌓 Toggle Theme</button>
<script>
  function toggleTheme() {
    document.body.classList.toggle('dark-theme');
    const isDark = document.body.classList.contains('dark-theme');
    localStorage.setItem('theme', isDark ? 'dark' : 'light');
  }
  // Check user's saved preference on page load
  if (localStorage.getItem('theme') === 'dark') {
    document.body.classList.add('dark-theme');
  }
</script>

<!-- ========================================== -->
<!-- 1 & 2. HERO SECTION (PHOTO, BUTTON, INTRO) -->
<!-- ========================================== -->
<div class="hero-container">
  
  <div class="hero-left">
    <img src="profile.jpg" alt="Sayak Bera" class="hero-img">
    <!-- Ensure your resume PDF is placed in the assets folder -->
    <a href="/assets/Sayak_Bera_Resume.pdf" download class="resume-btn action-btn">📄 Download Resume</a>
  </div>
  
  <div class="hero-right">
    <div>
      <h3 style="margin-top: 0; font-size: 1.8em; margin-bottom: 20px;">Namaskar! I am <strong>Sayak Bera</strong>.</h3>
      <p>I am a PhD Research Scholar at the <a href="https://www.cse.iitk.ac.in/index.html" style="text-decoration: none; font-weight: bold;">Computer Science & Engineering Department</a> of <a href="https://www.iitk.ac.in" style="text-decoration: none; font-weight: bold;">IIT Kanpur</a>, specializing in Space Borne Computation: Distributed ML Model Training & Earth Imaging based on Synthetic Aperture Radar (SAR).</p>
      <p>I am working under the supervision of Prof. <a href="https://www.cse.iitk.ac.in/users/amitangshu/" style="text-decoration: none; font-weight: bold;">Amitangshu Pal</a>.</p>
    </div>
    
    <div>
      <!-- This block is automatically pushed to align with the bottom of the resume button -->
      <p style="margin-bottom: 0;">My technical focus lies in deep learning and space borne computation, but this space is designed to capture all aspects of my work—from multi-GPU model training in the lab to the rhythms of Hindustani Classical music and the quiet moments captured through my camera lens.</p>
    </div>
  </div>
</div>

<!-- ========================================== -->
<!-- 3. CONTACT & SOCIALS                       -->
<!-- ========================================== -->
<div class="theme-card" style="display: flex; flex-direction: column; align-items: center; text-align: center; padding: 30px; background-color: #fcfcfc; border-radius: 12px; border: 1px solid #eaeaea; max-width: 600px; margin: 0 auto;">
  <h3 style="margin-top: 0; margin-bottom: 15px;">Get In Touch</h3>
  
  <p style="margin: 5px 0; line-height: 1.6;"><strong>Office:</strong> <br> Department of Computer Science & Engineering,<br>IIT Kanpur, Kanpur, UP 208016, India</p>
  
  <p style="margin: 15px 0 25px 0; line-height: 1.6;"><strong>Email:</strong> <br> <a href="mailto:sayakbera24@iitk.ac.in" style="text-decoration: none;">sayakbera24@iitk.ac.in</a> <br> <a href="mailto:sayakbera24@cse.iitk.ac.in" style="text-decoration: none;">sayakbera24@cse.iitk.ac.in</a></p>

  <div style="display: flex; gap: 30px; justify-content: center; align-items: center; flex-wrap: wrap;">
    <!-- Google Scholar -->
    <a href="https://scholar.google.com/citations?user=YOUR_ID" target="_blank" title="Google Scholar" style="color: #4285F4; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.1)'" onmouseout="this.style.transform='scale(1)'">
      <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="currentColor"><path d="M12 3L1 9l4 2.18v6L12 21l7-3.82v-6l2-1.09V17h2V9L12 3zm6.82 6L12 12.72 5.18 9 12 5.28 18.82 9zM17 15.99l-5 2.73-5-2.73v-3.72L12 15l5-2.73v3.72z"/></svg>
    </a>
    <!-- GitHub -->
    <a href="https://github.com/sayakbera24" target="_blank" title="GitHub" style="color: #181717; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.1)'" onmouseout="this.style.transform='scale(1)'">
      <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
    </a>
    <!-- LinkedIn -->
    <a href="https://linkedin.com/in/sayakbera24" target="_blank" title="LinkedIn" style="color: #0A66C2; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.1)'" onmouseout="this.style.transform='scale(1)'">
      <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="currentColor"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
    </a>
    <!-- YouTube -->
    <a href="http://www.youtube.com/@sayakrik" target="_blank" title="YouTube" style="color: #FF0000; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.1)'" onmouseout="this.style.transform='scale(1)'">
      <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="currentColor"><path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.5 12 3.5 12 3.5s-7.505 0-9.377.55a3.016 3.016 0 0 0-2.122 2.136C0 8.07 0 12 0 12s0 3.93.498 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.55 9.377.55 9.377.55s7.505 0 9.377-.55a3.016 3.016 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"/></svg>
    </a>
    <!-- Instagram -->
    <a href="https://instagram.com/atasmin_tad_buddhih" target="_blank" title="Instagram" style="color: #E1306C; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.1)'" onmouseout="this.style.transform='scale(1)'">
      <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
    </a>
    <!-- Facebook -->
    <a href="https://www.facebook.com/sayak.bera.50" target="_blank" title="Facebook" style="color: #1877F2; transition: transform 0.2s;" onmouseover="this.style.transform='scale(1.1)'" onmouseout="this.style.transform='scale(1)'">
      <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="currentColor"><path d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z"/></svg>
    </a>
  </div>
</div>

<!-- ========================================== -->
<!-- 4. HIGHLIGHTS & ACHIEVEMENTS               -->
<!-- ========================================== -->
<h2 class="section-header">Highlights</h2>
<ul class="list-container">
  <li>Spearheading active research into <strong>XAI-Based Detection of Adversarial Attacks</strong> on Deepfake Detectors.</li>
  <li>Architecting and managing <strong>multi-GPU computational environments</strong> for large-scale model training inside lab facilities.</li>
  <li>Managing instruction and evaluating complex submissions, including multiclass least squares problems, for a 40+ student cohort.</li>
  <li>Active practitioner of <strong>Hindustani Classical Music</strong>, maintaining regular vocal training and exploring complex Tabla rhythms.</li>
  <li>Curating an extensive local ornithology collection through <strong>Avian Photography</strong>.</li>
</ul>

<!-- ========================================== -->
<!-- 5. SELECTED PUBLICATIONS                   -->
<!-- ========================================== -->
<h2 class="section-header">Selected Publications</h2>
<ul class="list-container">
  <li>
    <span class="pub-title">Distributed ML Training Simulation in Space Borne Data Centers</span><br>
    <em>Sayak Bera, Amitangshu Pal, et al.</em> | <a href="#" style="text-decoration: none;">[View PDF]</a><br>
    Investigating 3D parallel training (Data, Pipeline, Tensor) to optimize cost and throughput using WAN.
  </li>
  <li>
    <span class="pub-title">Novel Hand-Crafted Image Descriptors for Enhanced Classification</span><br>
    <em>Sayak Bera, et al.</em> | <a href="#" style="text-decoration: none;">[View PDF]</a><br>
    Applying unique feature extraction to improve downstream classification metrics in computer vision models.
  </li>
  <li>
    <span class="pub-title">Evaluating XAI Robustness Against Adversarial Deepfake Attacks</span><br>
    <em>Sayak Bera, et al.</em> | <a href="#" style="text-decoration: none;">[View PDF]</a><br>
    Analyzing model behavior under white-box and black-box conditions including FGSM, BIM, C&W, and PGD.
  </li>
</ul>
