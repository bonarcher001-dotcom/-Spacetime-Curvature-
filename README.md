
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
            height: 60vh;
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

        /* Fixed Image Styling */
        .visual-aid {
            width: 100%;
            margin-top: 20px;
            text-align: center;
        }

        .visual-aid img {
            width: 100%;
            max-width: 700px;
            height: auto;
            border-radius: 12px;
            border: 2px solid #3a3a5e;
            box-shadow: 0 15px 35px rgba(0,0,0,0.8);
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
            transition: 0.3s;
        }
        
        button:hover {
            transform: translateY(-2px);
            background: #7c4dff;
        }
    </style>
</head>
<body>

    <div class="grid-bg"></div>

    <header>
        <h1>Spacetime</h1>
        <p style="font-size: 1.5rem;">Gravity is the geometry of the universe.</p>
        <button onclick="document.getElementById('learn').scrollIntoView({behavior: 'smooth'})">Start Learning</button>
    </header>

    <div class="container" id="learn">
        <section class="card">
            <h2>The Fabric of Reality</h2>
            <p>Think of space and time not as separate things, but as a single four-dimensional fabric. When a massive object like a star sits in this fabric, it creates a "dent." This dent is what we feel as <span class="highlight">gravity</span>.</p>
        </section>

        <section class="card">
            <h2>The Rubber Sheet Analogy</h2>
            <p>This is the most famous way to visualize general relativity. A heavy mass (the Sun) curves the grid, and smaller objects (planets) follow those curves.</p>
            
            <div class="visual-aid">
                <!-- Corrected Image Tag -->
                <img src="http://googleusercontent.com/image_collection/image_retrieval/93100428583492945" alt="Spacetime rubber sheet analogy diagram">
                <p style="color: #03dac6; font-size: 0.9rem; margin-top: 15px;">Diagram: How mass creates curvature in the spacetime grid.</p>
            </div>
        </section>

        <section class="card">
            <h2>Why This Matters</h2>
            <p>Without understanding this curvature, our technology wouldn't work. For example, <strong>GPS satellites</strong> have to account for the fact that time moves slightly differently in the "curved" space near Earth compared to deep space!</p>
        </section>
    </div>

    <footer>
        <p>&copy; 2026 Cosmic Education Project</p>
    </footer>

</body>
</html>
