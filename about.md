{% include header.html %}

<style>
/* Mobile-first styles */
.responsive-work-history-table {
  width: 100%;
  display: table !important;
  /* border-collapse: collapse; /* Not strictly needed for display:block */
}

.responsive-work-history-table th,
.responsive-work-history-table td {
  display: block; /* Stack table cells */
  width: 100% !important; /* Ensure full width */
  box-sizing: border-box; /* Consistent box model */
  padding: 0 0 1em 0; /* Space below each stacked item */
  text-align: left !important; /* Prefer left-align for stacked content */
}

/* Remove bottom padding from the very last cell in a table instance */
.responsive-work-history-table tr:last-child td:last-child {
  padding-bottom: 0;
}

/* Desktop and larger screen styles */
@media (min-width: 768px) { /* Adjust breakpoint as needed */
  .responsive-work-history-table {
    table-layout: fixed; /* Use fixed layout for precise column widths */
    border-collapse: collapse; /* Standard for tables */
  }

  .responsive-work-history-table th,
  .responsive-work-history-table td {
    display: table-cell; /* Revert to table cell behavior */
    width: auto !important; /* Reset mobile width */
    padding: 8px; /* Uniform padding for cells */
    vertical-align: top; /* Align content to the top */
    /* text-align will revert to default or can be set if needed */
  }

  /* First column (dates) */
  .responsive-work-history-table tr td:first-child { /* Applies to the date cell due to rowspan */
    width: 20% !important;
  }

  /* Second column (job title/description) */
  .responsive-work-history-table tr td:nth-child(2) { /* Applies to the title cell */
    width: 80% !important;
  }
  /* The description cell (in the second row) will automatically fall into the second column
     and adopt its width due to table-layout:fixed and the rowspan from the date cell. */
}

/* Styles for skill word cloud */
.skill-category-content {
  margin-top: 0.25em;
  margin-bottom: 1em; /* Space between categories */
  text-align: center; /* Center the content */
}
.skill-line {
  margin-bottom: 0.25em; /* Space between proficiency lines */
  line-height: 1.6; /* Adjust for better readability if skills wrap */
}
.skill-item {
  display: inline-block;
  padding: 0.2em 0.5em;
  margin: 0.2em;
  border-radius: 4px;
  background-color: #f0f0f0; /* Default background for items */
  line-height: 1.2; /* For the text inside the span */
  text-decoration: none; /* Remove underline if it's a link */
  color: #333; /* Default text color */
}
.skill-strong {
  font-size: 1.15em; /* Larger for strong */
  font-weight: 600;
  background-color: #ddeeff; /* Different bg for emphasis */
}
.skill-medium {
  font-size: 1.0em;
  font-weight: 500;
  background-color: #eef8ee;
}
.skill-light {
  font-size: 0.9em;
  font-weight: 400;
  color: #555;
  background-color: #f9f9f9;
}

.responsive-about-image-container {
  text-align: center;
  margin-top: 20px;
  margin-bottom: 30px;
}

.responsive-about-image {
  width: 100%;
  max-width: 700px; /* Adjust max-width as desired */
  aspect-ratio: 4/3;
  object-fit: cover;
  display: block;
  margin-left: auto;
  margin-right: auto;
  border-radius: 8px; /* Optional: for rounded corners */
}

@media (min-width: 768px) { /* Adjust breakpoint as needed */
  .responsive-about-image {
    aspect-ratio: 16/9;
    object-position: center top; /* Keeps the top portion, centered horizontally */
  }
}
</style>

# About

<div class="responsive-about-image-container">
  <img src="assets/images/iceland_mountain.jpg" alt="Me after climbing most of Akrafjall" class="responsive-about-image" />
  <p style="font-style: italic; margin-top: 10px; font-size: 0.9em;">Me after climbing most of <a href="https://maps.app.goo.gl/GhhZUYdnHckaFV4K9">Akrafjall</a></p>
</div>

I am an audio software engineer and researcher from the UK, with a PhD in Artificial Intelligence and Music. With over a decade of experience spanning DSP algorithm development, embedded systems, and pioneering work in AI/ML for audio, I am passionate about translating complex signal processing and machine learning concepts into innovative real-world applications for the creative industries and beyond.

My background includes bringing numerous products in professional and consumer electronics to fruition, from active noise-cancelling headphones and video encoders to guitar/bass amplifiers. My recent research in edge AI, including the development of the **MEML** framework for on-device training, has deepened my focus on the potential and challenges of deploying small, efficient AI models for real-time signal manipulation and gesture recognition. The **HITar**, an AI-augmented acoustic guitar and international award winner, exemplifies my commitment to designing responsive, intimate, and cutting-edge musical interactions. I thrive on leveraging deep technical expertise to create impactful and engaging user experiences.

## 💼 Recent Work History


<table class="responsive-work-history-table">
<tr>
<td rowspan=2><strong>June 2024<br>Present (end Oct 2025)</strong></td>
<td><strong>University of Sussex</strong> – Brighton, UK<br><strong>Research Fellow in Musical Instrument Design and Creative Machine Learning</strong></td>
</tr>
<tr>
<td>
<ul>
<li>Research <a href="projects.html#meml">Musically Embodied Machine Learning</a> and train AI models through musical interfaces in real time on RP2350 and XMOS Xcore.ai embedded platforms.</li>
<li>Create <a href="https://github.com/MusicallyEmbodiedML/memlp"><strong>meMLP</strong></a>, an edge AI library with support for RL and on-device training.</li>
</ul>
</td>
</tr>
</table>

<br> <!-- Add some space between tables -->

<table class="responsive-work-history-table">
<tr>
<td rowspan=2><strong>September 2023<br>Present (end Jul 2025)</strong></td>
<td><strong>Queen Mary University of London</strong> – London, UK<br><strong>Research Assistant – Impact Fund grant “HITar”</strong></td>
</tr>
<tr>
<td>
<ul>
<li>Spearhead commercialisation of the <a href="projects.html#HITar">HITar</a>: protect IP, devise business model and sales funnel, and drive customer engagement.</li>
<li>Exhibit the HITar at trade shows (Music China 2023, NAMM 2024).</li>
</ul>
</td>
</tr>
</table>

<br> <!-- Add some space between tables -->

<table class="responsive-work-history-table">
<tr>
<td rowspan=2><strong>September 2017<br>December 2019</strong></td>
<td><strong>ams AG (Semiconductors and sensors)</strong> – Stokenchurch, UK<br><strong>Digital Signal Processor Software Engineer</strong></td>
</tr>
<tr>
<td>
<ul>
<li>Implement adaptive hybrid Active Noise Cancellation (ANC) algorithms.</li>
<li>Develop Automatic Leakage Compensation on the proprietary <a href="https://ams-osram.com/products/sensor-solutions/active-noise-cancellation/ams-as3460">AS3460 chip</a>.</li>
<li>Drive product development from research simulation to finished product within one year, collaborating closely with acoustical engineering.</li>
</ul>
</td>
</tr>
</table>

<br> <!-- Add some space between tables -->

<table class="responsive-work-history-table">
<tr>
<td rowspan=2><strong>March 2015<br>September 2017</strong></td>
<td><strong>Blackstar Amplification Ltd</strong> – Northampton, UK<br><strong>DSP Engineer</strong></td>
</tr>
<tr>
<td>
<ul>
<li>Conduct R&D of non-linear digital audio processing algorithms.</li>
<li>Bring impactful products to market:
    <ul>
    <li><a href="https://blackstaramps.com/idcore-v4/">ID:Core</a> digital amps: polyphonic octaver, looper, chorus/flanger, envelope filter.</li>
    <li><a href="https://blackstaramps.com/ht-venue-mkii/">Venue MkII</a> hybrid amps: reverb, power amp simulation.</li>
    <li><a href="https://blackstaramps.com/unity/">Unity</a> bass amps: completely new design, bass distortion simulator, feedback compressor.</li>
    </ul>
</li>
</ul>
</td>
</tr>
</table>

<br> <!-- Add some space between tables -->

<table class="responsive-work-history-table">
<tr>
<td rowspan=2><strong>October 2013<br>March 2015</strong></td>
<td><strong>ITDev Ltd</strong> – Southampton, UK<br><strong>Graduate Software Engineer</strong></td>
</tr>
<tr>
<td>
<ul>
<li>Develop software projects using PHP, Python, JS, Perl, and embedded C.</li>
<li>Serve as SCRUM master.</li>
<li>Embedded development on video encoder systems.</li>
</ul>
</td>
</tr>
</table>

## 🛠️ Skills and Achievements

**Languages:**
<div class="skill-category-content">
  <div class="skill-line"><span class="skill-item skill-strong">C++</span> <span class="skill-item skill-strong">C</span> <span class="skill-item skill-strong">Python</span> <span class="skill-item skill-strong">ARM Assembly</span></div>
  <div class="skill-line"><span class="skill-item skill-medium">Javascript</span> <span class="skill-item skill-medium">PHP</span> <span class="skill-item skill-medium">Perl</span></div>
  <div class="skill-line"><span class="skill-item skill-light">Ruby</span> <span class="skill-item skill-light">Rust</span> <span class="skill-item skill-light">Coffeescript</span></div>
</div>

**Hardware platforms:**
<div class="skill-category-content">
  <div class="skill-line"><span class="skill-item skill-strong">ARM Cortex-M</span> <span class="skill-item skill-strong">XMOS</span> <span class="skill-item skill-strong">x86</span></div>
  <div class="skill-line"><span class="skill-item skill-medium">Xtensa HiFi3</span> <span class="skill-item skill-medium">ARM Cortex-A</span> <span class="skill-item skill-medium">SHARC</span></div>
  <!-- Add a skill-light line if there are any hardware platforms with little experience -->
</div>

**AI platforms**
<div class="skill-category-content">
  <div class="skill-line"><span class="skill-item skill-strong">Pytorch</span> <span class="skill-item skill-strong">Torchlib</span></div>
  <div class="skill-line"><span class="skill-item skill-medium">Keras</span> <span class="skill-item skill-medium">ONNX</span> <span class="skill-item skill-medium">TFLite-micro</span></div>
  <!-- Add a skill-light line if there are any AI platforms with little experience -->
</div>

* **DSP Concepts:**
  * Fixed-point signal chains
  * Filtered-X LMS
  * Optimised fixed-point STFT
  * Multi-rate processing

* **Audio Effects:**
  * Pitch shifting, reverb, fuzz
  * Model analogue gain stages
  * Feedback/feed-forward compressors
  * Complex real-time chains on constrained DSPs
* **Toolchains & Testing:**
  * Unit testing: microunit, catch2, unity
  * Continuous integration: Jenkins
  * Automated DSP testing with CI pipelines
  * Native C++ &leftrightarrow; Python integration via Boost::Python, PyBind11

* **ML/AI Concepts:**
  * ML from scratch in embedded C++: backpropagation, optimisation
  * CNNs, CRNNs, VAEs in embedded real-time AI
  * Reinforcement learning: deep deterministic policy gradient (DDPG)
  * Multi-threaded deployment into VST, Max/MSP, ARM-based edge platforms

* **Acoustics:**
  * FF/FB noise cancellation
  * Room modelling (FDTD, FEM, Digital Waveguide)
  * Spatial hearing and psychoacoustics
  * Acoustic simulation: MATLAB, CATT-Acoustic, COMSOL

---

## 🎓 Education and Qualifications

### PhD Artificial Intelligence and Music
**Queen Mary University of London, Centre for Digital Music**
*September 2019 – April 2025*

*   *Thesis:* “Augmenting an acoustic guitar for percussive fingerstyle”

---

### MSc Sound and Vibration Studies *(with Merit)*
**University of Southampton, Institute of Sound and Vibration Research**
*September 2012 – September 2013*

*   *Dissertation:* Refining an FDTD acoustic model for room auralisation with OPSODIS Ltd

---

### BSc Informatica Musicale (Musical Information Technology)
**Università degli Studi di Milano**
*September 2009 – September 2012*

*   *Grade:* 110/110 cum laude
*   *Dissertation:* Further evidences of the contribution of the ear canal to directional hearing

---

## 🏊 Other Interests

* Extrovert and excellent communicator, confident in public speaking.
* Keen cyclist, swimmer, runner; passionate cook.

---

## 📚 Publications

Martelloni, A. and Kiefer, C., 2024. Musically Embedded Machine Learning (MEML) Demo. In CHIME 2024

Kiefer, C. and Martelloni, A., 2024. Musically Embedded Machine Learning Workshop. In CHIME 2024

Armitage, J., Shepardson, V., Privato, N., Pelinski, T., Benito Temprano, A.L., Wolstanholme, L., Martelloni, A., Caspe, F.S., Reed, C.N., Skach, S. and Diaz, R., 2023, August. Agential Instruments Design Workshop. 4th International Conference on AI and Music Creativity (AIMC).

Martelloni, A., McPherson, A. and Barthet, M., 2023, November. Real-Time Percussive Technique Recognition and Embedding Learning for the Acoustic Guitar. In ISMIR 2023

Reed, C.N., Nordmoen, C., Martelloni, A., Lepri, G., Robson, N., Zayas-Garin, E., Cotton, K. and McPherson, A., 2022, June. Exploring experiences with new musical instruments through micro-phenomenology. In NIME 2022.

Martelloni, A., McPherson, A. and Barthet, M., 2021, April. Guitar augmentation for Percussive Fingerstyle: Combining self-reflexive practice and user-centred design. In NIME 2021.

Martelloni, A., McPherson, A. and Barthet, M., 2020. Percussive Fingerstyle Guitar through the Lens of NIME: an Interview Study. In NIME 2020.

Martelloni, A., Mauro, D.A. and Mancuso, A., 2013, June. Further evidences of the contribution of the ear canal to directional hearing: design of a compensation filter. In Proceedings of Meetings on Acoustics (Vol. 19, No. 1). AIP Publishing.
