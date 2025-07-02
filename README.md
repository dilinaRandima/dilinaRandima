<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dilina Randima | Full Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2d2b55;
            --secondary: #6c63ff;
            --accent: #ff6584;
            --light: #f8f9fa;
            --dark: #1a1a2e;
            --gray: #6c757d;
            --card-bg: rgba(255, 255, 255, 0.08);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, var(--dark), #16213e);
            color: var(--light);
            line-height: 1.6;
            padding: 2rem;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
            padding-top: 1rem;
        }

        .profile-pic {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid var(--secondary);
            margin: 0 auto 1.5rem;
            background: linear-gradient(45deg, var(--secondary), var(--accent));
            position: relative;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 4rem;
        }

        h1 {
            font-size: 2.8rem;
            margin-bottom: 0.5rem;
            background: linear-gradient(45deg, var(--secondary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
        }

        .tagline {
            font-size: 1.4rem;
            color: #d0d0e7;
            max-width: 800px;
            margin: 0 auto 1.5rem;
        }

        .badges {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin: 1.5rem 0;
            flex-wrap: wrap;
        }

        .badge {
            background: var(--card-bg);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(108, 99, 255, 0.2);
        }

        .badge i {
            color: var(--secondary);
        }

        .content-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .card {
            background: var(--card-bg);
            border-radius: 15px;
            padding: 1.8rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(108, 99, 255, 0.1);
            transition: var(--transition);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .card:hover {
            transform: translateY(-10px);
            border-color: rgba(108, 99, 255, 0.4);
        }

        .card h2 {
            font-size: 1.6rem;
            margin-bottom: 1.5rem;
            color: var(--secondary);
            display: flex;
            align-items: center;
            gap: 0.8rem;
        }

        .card h2 i {
            background: rgba(108, 99, 255, 0.2);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }

        .stat-card {
            background: rgba(26, 26, 46, 0.5);
            padding: 1.2rem;
            border-radius: 10px;
            text-align: center;
            transition: var(--transition);
        }

        .stat-card:hover {
            background: rgba(108, 99, 255, 0.2);
            transform: scale(1.05);
        }

        .stat-value {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 0.3rem;
            color: var(--secondary);
        }

        .stat-label {
            font-size: 0.9rem;
            color: #a0a0c0;
        }

        .languages {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .language-bar {
            background: rgba(255, 255, 255, 0.1);
            height: 10px;
            border-radius: 5px;
            overflow: hidden;
            position: relative;
        }

        .language-fill {
            height: 100%;
            border-radius: 5px;
        }

        .language-info {
            display: flex;
            justify-content: space-between;
            font-size: 0.95rem;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(70px, 1fr));
            gap: 1.2rem;
            margin-top: 1rem;
        }

        .tech-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.5rem;
            transition: var(--transition);
        }

        .tech-icon {
            width: 60px;
            height: 60px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            transition: var(--transition);
        }

        .tech-item:hover .tech-icon {
            background: rgba(108, 99, 255, 0.3);
            transform: translateY(-5px);
        }

        .tech-name {
            font-size: 0.8rem;
            text-align: center;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-top: 2rem;
        }

        .social-btn {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--card-bg);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: var(--light);
            transition: var(--transition);
            border: 1px solid rgba(108, 99, 255, 0.2);
        }

        .social-btn:hover {
            background: var(--secondary);
            transform: translateY(-5px);
        }

        .streak-container {
            display: flex;
            justify-content: space-between;
            margin-top: 1.5rem;
            gap: 1rem;
        }

        .streak-card {
            flex: 1;
            background: rgba(26, 26, 46, 0.5);
            padding: 1.2rem;
            border-radius: 10px;
            text-align: center;
        }

        .streak-value {
            font-size: 2rem;
            font-weight: 700;
            margin: 0.5rem 0;
            color: var(--accent);
        }

        .streak-label {
            color: #a0a0c0;
            font-size: 0.9rem;
        }

        .streak-dates {
            font-size: 0.85rem;
            color: #c0c0e0;
            margin-top: 0.3rem;
        }

        .fun-fact {
            background: rgba(255, 101, 132, 0.1);
            border-left: 4px solid var(--accent);
            padding: 1.2rem;
            border-radius: 0 10px 10px 0;
            margin-top: 1.5rem;
            font-style: italic;
        }

        @media (max-width: 768px) {
            .content-grid {
                grid-template-columns: 1fr;
            }
            
            .streak-container {
                flex-direction: column;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .tagline {
                font-size: 1.1rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="profile-pic">
                <i class="fas fa-user"></i>
            </div>
            <h1>Dilina Randima</h1>
            <p class="tagline">Full Stack Developer specializing in the MERN stack. Building scalable web applications and turning creative ideas into reality through code.</p>
            
            <div class="badges">
                <div class="badge">
                    <i class="fas fa-eye"></i>
                    <span>Profile Views: 72</span>
                </div>
                <div class="badge">
                    <i class="fas fa-envelope"></i>
                    <span>dilinarandima333@gmail.com</span>
                </div>
            </div>
        </header>

        <div class="content-grid">
            <!-- About Section -->
            <div class="card">
                <h2><i class="fas fa-user"></i> About Me</h2>
                <p>I'm a passionate Full Stack Developer specializing in the MERN stack (MongoDB, Express.js, React.js, Node.js).</p>
                
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-value">72</div>
                        <div class="stat-label">Total Contributions</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">51</div>
                        <div class="stat-label">2025 Commits</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">13</div>
                        <div class="stat-label">Total PRs</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value">0</div>
                        <div class="stat-label">Total Issues</div>
                    </div>
                </div>
                
                <div class="streak-container">
                    <div class="streak-card">
                        <div class="streak-value">4</div>
                        <div class="stat-label">Current Streak</div>
                        <div class="streak-dates">Jul 2</div>
                    </div>
                    <div class="streak-card">
                        <div class="streak-value">4</div>
                        <div class="stat-label">Longest Streak</div>
                        <div class="streak-dates">May 4 - May 7</div>
                    </div>
                </div>
                
                <div class="fun-fact">
                    <i class="fas fa-lightbulb"></i> Fun fact: My favorite programming language? Whichever one isn't throwing errors today.
                </div>
            </div>

            <!-- Languages Section -->
            <div class="card">
                <h2><i class="fas fa-code"></i> Languages</h2>
                <div class="languages">
                    <div>
                        <div class="language-info">
                            <span>JavaScript</span>
                            <span>55.07%</span>
                        </div>
                        <div class="language-bar">
                            <div class="language-fill" style="background: #6c63ff; width: 55.07%"></div>
                        </div>
                    </div>
                    
                    <div>
                        <div class="language-info">
                            <span>CSS</span>
                            <span>35.70%</span>
                        </div>
                        <div class="language-bar">
                            <div class="language-fill" style="background: #ff6584; width: 35.70%"></div>
                        </div>
                    </div>
                    
                    <div>
                        <div class="language-info">
                            <span>Java</span>
                            <span>8.93%</span>
                        </div>
                        <div class="language-bar">
                            <div class="language-fill" style="background: #00c9a7; width: 8.93%"></div>
                        </div>
                    </div>
                    
                    <div>
                        <div class="language-info">
                            <span>HTML</span>
                            <span>0.29%</span>
                        </div>
                        <div class="language-bar">
                            <div class="language-fill" style="background: #ffde7d; width: 0.29%"></div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Technologies Section -->
            <div class="card">
                <h2><i class="fas fa-tools"></i> Technologies</h2>
                <div class="tech-grid">
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-js"></i>
                        </div>
                        <span class="tech-name">JavaScript</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-react"></i>
                        </div>
                        <span class="tech-name">React</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-node-js"></i>
                        </div>
                        <span class="tech-name">Node.js</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fas fa-database"></i>
                        </div>
                        <span class="tech-name">MongoDB</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-css3-alt"></i>
                        </div>
                        <span class="tech-name">CSS</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-html5"></i>
                        </div>
                        <span class="tech-name">HTML</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-java"></i>
                        </div>
                        <span class="tech-name">Java</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-python"></i>
                        </div>
                        <span class="tech-name">Python</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fas fa-server"></i>
                        </div>
                        <span class="tech-name">Express</span>
                    </div>
                    <div class="tech-item">
                        <div class="tech-icon">
                            <i class="fab fa-git-alt"></i>
                        </div>
                        <span class="tech-name">Git</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Connect Section -->
        <div class="card">
            <h2><i class="fas fa-handshake"></i> Connect with Me</h2>
            <div class="social-links">
                <a href="#" class="social-btn">
                    <i class="fab fa-github"></i>
                </a>
                <a href="#" class="social-btn">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="#" class="social-btn">
                    <i class="fab fa-twitter"></i>
                </a>
                <a href="#" class="social-btn">
                    <i class="fas fa-envelope"></i>
                </a>
            </div>
        </div>
    </div>

    <script>
        // Animation for stats counter
        document.addEventListener('DOMContentLoaded', function() {
            const statCards = document.querySelectorAll('.stat-card');
            
            statCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    const valueElement = this.querySelector('.stat-value');
                    const finalValue = parseInt(valueElement.textContent);
                    let currentValue = 0;
                    
                    const counter = setInterval(() => {
                        if (currentValue < finalValue) {
                            currentValue += Math.ceil(finalValue / 20);
                            if (currentValue > finalValue) currentValue = finalValue;
                            valueElement.textContent = currentValue;
                        } else {
                            clearInterval(counter);
                        }
                    }, 50);
                });
            });
        });
    </script>
</body>
</html>
