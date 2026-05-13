<main class="left card">
  <canvas id="sim"></canvas>

  <div class="controls">
    <label>Mass: <input id="massRange" type="range" min="50" max="2000" value="400"></label>
    <label>Gravity Strength: <input id="gRange" type="range" min="0.1" max="4" step="0.1" value="1"></label>
    <label>Friction: <input id="dampRange" type="range" min="0" max="0.2" step="0.01" value="0.02"></label>
    <button id="resetBtn" class="btn">Reset Particles</button>
    <div class="legend">Click the canvas to add a particle. Drag the mass (big dot). Right-click a particle to remove it.</div>
  </div>

  <div class="section">
    <h3 style="margin:6px 0 8px;">How to use</h3>
    <ul style="margin:0 0 8px 18px; color:var(--muted)">
      <li>Drag the central mass (large yellow dot) to move the curvature center.</li>
      <li>Click to add test particles with initial velocity pointing away from click position.</li>
      <li>Adjust mass and gravity strength to see deeper or shallower wells.</li>
    </ul>
    <h3 style="margin:6px 0 6px;">Notes on analogy</h3>
    <p style="color:var(--muted); margin:0;">This 2D "fabric" and particle simulator is a visualization/analogy. General Relativity describes curvature in four-dimensional spacetime; this demo captures the qualitative idea that mass tells spacetime how to curve and curvature tells matter how to move.</p>
  </div>
</main>

<aside class="right card">
  <div class="section">
    <h3>Key Equations</h3>
    <pre>Einstein field eq: Gμν + Λgμν = (8πG/c⁴) Tμν
