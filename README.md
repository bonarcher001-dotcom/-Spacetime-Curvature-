
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Understanding Spacetime Curvature</title>
    <style>
        /* Base Styling */
        body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #05050a;
            color: #e0e0e0;
            line-height: 1.6;
        }

        /* Spacetime Grid Background Effect */
        .grid-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(100, 100, 255, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(100, 100, 255, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            z-index: -1;
        }

        header {
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
        }

        h1 {
            font-size: 4rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #6200ea, #03dac6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        .card {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 30px;
            backdrop-filter: blur(10px);
        }

        .highlight {
            color: #03dac6;
            font-weight: bold;
        }

        /* Interactive Element Placeholder (modified to hold SVG) */
        .simulation-box {
            width: 100%;
            background: #000;
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            border: 2px dashed #3a3a5e;
            cursor: pointer;
            transition: 0.3s;
            margin-top: 20px;
            padding: 20px;
            box-sizing: border-box;
        }

        .simulation-box:hover {
            border-color: #6200ea;
            background: #0a0a1a;
        }

        footer {
            text-align: center;
            padding: 40px;
            font-size: 0.9rem;
            color: #777;
        }

        button {
            background: #6200ea;
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 30px;
            font-size: 1rem;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(98, 0, 234, 0.3);
        }

        /* SVG Specific Styling */
        svg {
            width: 100%;
            height: auto;
            max-width: 800px; /* Optional cap */
        }
    </style>
</head>
<body>

    <div class="grid-bg"></div>

    <header>
        <h1>Spacetime</h1>
        <p style="font-size: 1.5rem;">The fabric of the universe is not a void; it’s a stage.</p>
        <button onclick="document.getElementById('learn').scrollIntoView({behavior: 'smooth'})">Begin the Journey</button>
    </header>

    <div class="container" id="learn">
        <section class="card">
            <h2>What is Curvature?</h2>
            <p>In 1915, Albert Einstein realized that space and time are linked in a four-dimensional fabric called <span class="highlight">spacetime</span>. Gravity isn't just a "pull" between objects; it is the warping of this fabric caused by mass.</p>
            <blockquote>"Matter tells space how to curve; space tells matter how to move." — John Wheeler</blockquote>
        </section>

        <section class="card">
            <h2>The Trampoline Analogy</h2>
            <p>Imagine placing a bowling ball on a trampoline. The fabric dips. If you roll a marble nearby, it won't move in a straight line—it will follow the <span class="highlight">curve</span> created by the bowling ball. This is exactly how planets orbit stars.</p>
            
            <div class="simulation-box">
                <!-- Inline SVG Visualization -->
                <svg viewBox="0 0 800 500" xmlns="http://www.w3.org/2000/svg">
                    <!-- Background Grid -->
                    <defs>
                        <pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse">
                            <path d="M 40 0 L 0 0 0 40" fill="none" stroke="rgba(100, 100, 255, 0.3)" stroke-width="1"/>
                        </pattern>
                    </defs>
                    <rect width="800" height="500" fill="url(#grid)" />

                    <!-- Distorted Mesh Central Dip -->
                    <path d="M 0 250 Q 200 250 350 350 L 450 350 Q 600 250 800 250" fill="none" stroke="rgba(100, 100, 255, 0.6)" stroke-width="2"/>
                    <path d="M 400 0 L 400 150 Q 400 350 400 500" fill="none" stroke="rgba(100, 100, 255, 0.6)" stroke-width="2"/>
                    <ellipse cx="400" cy="350" rx="150" ry="80" fill="none" stroke="rgba(100, 100, 255, 0.6)" stroke-width="2" transform="rotate(-15 400 350)"/>
                    
                    <!-- Massive Object (Bowling Ball) -->
                    <circle cx="400" cy="350" r="60" fill="#202020" stroke="#03dac6" stroke-width="4"/>
                    
                    <!-- Labels -->
                    <text x="400" y="355" font-family="Segoe UI" font-size="16" fill="white" text-anchor="middle">Mass (Sun)</text>
                    <text x="250" y="220" font-family="Segoe UI" font-size="14" fill="#a0a0c0">Space-Time Grid (Rubber Sheet)</text>
                    
                    <!-- Distortion Callout -->
                    <line x1="330" y1="360" x2="280" y2="420" stroke="white" stroke-width="1" marker-end="url(#arrowhead)"/>
                    <text x="280" y="440" font-family="Segoe UI" font-size="14" fill="white" text-anchor="middle">Curvature</text>

                    <!-- Test Mass Path -->
                    <circle cx="100" cy="200" r="8" fill="#e0e0e0"/>
                    <path d="M 100 200 C 200 200, 300 300, 380 345" fill="none" stroke="white" stroke-width="2" stroke-dasharray="5,5"/>
                    <text x="90" y="185" font-family="Segoe UI" font-size="14" fill="#e0e0e0">Test Mass (e.g., Planet)</text>
                    
                    <!-- Test Mass Velocity Arrow -->
                    <line x1="108" y1="200" x2="160" y2="200" stroke="#03dac6" stroke-width="2" marker-end="url(#arrowhead-green)"/>
                    
                    <!-- Comparison Insets -->
                    <g transform="translate(600, 50) scale(0.6)">
                        <rect width="250" height="150" fill="#000" stroke="rgba(255, 255, 255, 0.1)" stroke-width="2"/>
                        <rect width="250" height="150" fill="url(#grid)" />
                        <line x1="20" y1="75" x2="230" y2="75" stroke="#e0e0e0" stroke-width="2" stroke-dasharray="5,5"/>
                        <text x="125" y="165" font-family="Segoe UI" font-size="20" fill="white" text-anchor="middle">Flat Space (Empty)</text>
                    </g>
                    <g transform="translate(600, 250) scale(0.6)">
                        <rect width="250" height="150" fill="#000" stroke="rgba(255, 255, 255, 0.1)" stroke-width="2"/>
                        <rect width="250" height="150" fill="url(#grid)" />
                        <path d="M 20 75 Q 125 125 230 75" fill="none" stroke="#e0e0e0" stroke-width="2" stroke-dasharray="5,5"/>
                        <text x="125" y="165" font-family="Segoe UI" font-size="20" fill="white" text-anchor="middle">Curved Space (Near Mass)</text>
                    </g>

                    <!-- Definitions for Arrows -->
                    <defs>
                        <marker id="arrowhead" markerWidth="10" markerHeight="7" refX="0" refY="3.5" orient="auto">
                            <polygon points="0 0, 10 3.5, 0 7" fill="white"/>
                        </marker>
                        <marker id="arrowhead-green" markerWidth="10" markerHeight="7" refX="0" refY="3.5" orient="auto">
                            <polygon points="0 0, 10 3.5, 0 7" fill="#03dac6"/>
                        </marker>
                    </defs>
                </svg>
                <p style="text-align: center; color: #777; margin-top: 10px;">Visualize Mass vs. Curvature (Click to interact, once enabled)</p>
            </div>
        </section>

        <section class="card">
            <h2>Real-World Evidence</h2>
            <ul>
                <li><strong>Gravitational Lensing:</strong> Light from distant stars bends as it passes near the Sun.</li>
                <li><strong>GPS Correction:</strong> Clocks on satellites move slightly faster than those on Earth because they are further from the Earth's "dent" in spacetime.</li>
            </ul>
        </section>
    </div>

    <footer>
        <p>&copy; 2026 Cosmic Education Project</p>
    </footer>

</body>
</html>
