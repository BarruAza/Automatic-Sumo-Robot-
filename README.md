<h1>🤖 SmartWatt Sumo Robot – Final Project (Sistem Automasi)</h1>

<p>
  This project implements a <strong>Sumo Robot</strong> powered by <strong>ESP32</strong> with a PID-oriented control flow. 
  The robot uses an <strong>HC-SR04 ultrasonic sensor</strong> to detect opponents and <strong>IR sensors</strong> to read arena boundaries. 
  A <strong>Finite State Machine (FSM)</strong> governs the robot’s behavior, enabling it to attack, defend, or retreat in real time.
</p>

<p>🎥 <strong>Demo &amp; Presentation:</strong></p>
<ul>
  <li><a href="https://www.youtube.com/watch?v=8qFzm3vdtHY" target="_blank" rel="noopener">Presentation Video</a></li>
  <li><a href="https://youtu.be/-q4ZjlIR-U4?si=6y-QIw76LEkfft7m" target="_blank" rel="noopener">Demo Video</a></li>
</ul>

<hr />

<h2>⚡ Features</h2>
<ul>
  <li>Real-time opponent detection with <strong>HC-SR04 ultrasonic sensor</strong>.</li>
  <li><strong>IR sensors</strong> for edge detection and safe maneuvering.</li>
  <li>FSM-controlled behavior with states: <code>IDLE</code>, <code>FORWARD</code>, <code>ATTACK</code>, <code>AVOID_EDGE_FRONT</code>, <code>AVOID_EDGE_BACK</code>.</li>
  <li>Automatic &amp; defensive braking logic.</li>
  <li>Motor control via <strong>PWM</strong> for smooth speed management.</li>
</ul>

<h2>🛠️ Hardware Requirements</h2>
<ul>
  <li>ESP32 Devkit V1</li>
  <li>L298N Motor Driver</li>
  <li>2 × DC Motors</li>
  <li>HC-SR04 Ultrasonic Sensor</li>
  <li>2 × IR Sensors (Front &amp; Rear)</li>
  <li>Li-Po Battery 3.7V + Step-Up Converter 5V</li>
  <li>LED Indicator &amp; Push Button</li>
  <li>Breadboard, capacitors, and wiring</li>
</ul>

<h2>🧩 Software Requirements</h2>
<ul>
  <li>Arduino IDE / PlatformIO</li>
  <li>Language: <strong>C++ (Arduino Framework)</strong></li>
  <li>Core libs:
    <ul>
      <li><code>Arduino.h</code> (built-in)</li>
      <li><code>driver/ledc.h</code> (ESP32 PWM)</li>
    </ul>
  </li>
</ul>

<h2>📂 Repository Structure</h2>
<pre><code>SUMO-ROBOT/
├─ docs/               # Documentation and project report
├─ src/                # ESP32 source code
│  └─ main.ino
├─ media/              # Photos, videos, demo files
├─ LICENSE
└─ README.md           # Project description
</code></pre>

<h2>🚀 How to Run</h2>
<ol>
  <li>Clone this repository:</li>
</ol>
<pre><code>git clone https://github.com/username/SUMO-ROBOT.git
</code></pre>
<ol start="2">
  <li>Open <code>src/main.ino</code> in Arduino IDE (or PlatformIO).</li>
  <li>Select <strong>ESP32 Devkit V1</strong> as the board.</li>
  <li>Connect the hardware as per schematic and upload the sketch.</li>
  <li>Power the robot and test in the sumo arena.</li>
</ol>

<h2>🧠 FSM Overview</h2>
<ul>
  <li><code>STATE_IDLE</code> – Wait state.</li>
  <li><code>STATE_FORWARD</code> – Default forward movement.</li>
  <li><code>STATE_ATTACK</code> – Move forward aggressively when an opponent is detected.</li>
  <li><code>STATE_AVOID_EDGE_FRONT</code> – Stop, reverse, and rotate when the front IR sees the boundary.</li>
  <li><code>STATE_AVOID_EDGE_BACK</code> – Push forward hard to avoid being pushed out when rear IR detects the edge.</li>
</ul>

<h2>👨‍💻 Team Members (Group 6)</h2>
<ul>
  <li>Ruasa Azizan Zihni – Hardware &amp; Testing</li>
  <li>Barru Wira Yasa – Programming &amp; Debugging</li>
  <li>Ibadurahman Faiz Usman – System Integration</li>
  <li>Rayhan Sulistyawan – System Testing &amp; Analysis</li>
  <li>Dzaki Rabbani – Documentation</li>
  <li>M. Radhi Rasyidi Rafli – Documentation &amp; Presentation</li>
</ul>

<h2>📚 References</h2>
<ul>
  <li><a href="https://cdn.sparkfun.com/datasheets/Sensors/Proximity/HCSR04.pdf" target="_blank" rel="noopener">HC-SR04 Ultrasonic Sensor Datasheet</a></li>
  <li><a href="https://www.ti.com/lit/ds/symlink/l293.pdf" target="_blank" rel="noopener">L298/L293 Motor Driver (TI)</a></li>
  <li><a href="https://docs.espressif.com/" target="_blank" rel="noopener">ESP32 Official Documentation</a></li>
</ul>

<hr />
