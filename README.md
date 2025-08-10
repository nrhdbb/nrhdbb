<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Project README</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="0.5"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(2deg); }
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .logo {
            width: 120px;
            height: 120px;
            background: linear-gradient(135deg, #ff6b6b, #feca57);
            border-radius: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 30px;
            font-size: 48px;
            animation: pulse 2s ease-in-out infinite;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            color: white;
            margin-bottom: 20px;
            text-shadow: 0 4px 20px rgba(0,0,0,0.3);
            animation: slideInUp 1s ease-out;
        }

        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero p {
            font-size: 1.5rem;
            color: rgba(255,255,255,0.9);
            margin-bottom: 40px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            animation: slideInUp 1s ease-out 0.2s both;
        }

        .badges {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
            margin-bottom: 40px;
            animation: slideInUp 1s ease-out 0.4s both;
        }

        .badge {
            background: rgba(255,255,255,0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.3);
            padding: 8px 16px;
            border-radius: 25px;
            color: white;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            font-size: 0.9rem;
        }

        .badge:hover {
            background: rgba(255,255,255,0.3);
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }

        .cta-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            animation: slideInUp 1s ease-out 0.6s both;
        }

        .btn {
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1rem;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .btn-primary {
            background: linear-gradient(135deg, #ff6b6b, #feca57);
            color: white;
            box-shadow: 0 10px 30px rgba(255,107,107,0.3);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 35px rgba(255,107,107,0.4);
        }

        .btn-secondary {
            background: rgba(255,255,255,0.2);
            color: white;
            border: 2px solid rgba(255,255,255,0.3);
            backdrop-filter: blur(10px);
        }

        .btn-secondary:hover {
            background: rgba(255,255,255,0.3);
            transform: translateY(-3px);
        }

        /* Main Content */
        .main-content {
            background: white;
            position: relative;
            z-index: 3;
            margin-top: -100px;
            border-radius: 30px 30px 0 0;
            box-shadow: 0 -10px 40px rgba(0,0,0,0.1);
        }

        .section {
            padding: 80px 0;
            border-bottom: 1px solid #f0f0f0;
        }

        .section:last-child {
            border-bottom: none;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-header h2 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 15px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .section-header p {
            font-size: 1.2rem;
            color: #666;
            max-width: 600px;
            margin: 0 auto;
        }

        /* Features Grid */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .feature-card {
            background: #f8f9ff;
            padding: 40px 30px;
            border-radius: 20px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid #e8ecff;
            position: relative;
            overflow: hidden;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(135deg, #667eea, #764ba2);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(102,126,234,0.15);
        }

        .feature-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 2rem;
            color: white;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 15px;
            color: #333;
        }

        /* Installation Steps */
        .install-steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .install-step {
            background: #fff;
            border: 2px solid #f0f0f0;
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            position: relative;
            transition: all 0.3s ease;
        }

        .install-step:hover {
            border-color: #667eea;
            transform: translateY(-5px);
        }

        .step-number {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 600;
        }

        /* Code Block */
        .code-block {
            background: #1a1a1a;
            color: #f8f8f2;
            padding: 30px;
            border-radius: 15px;
            margin: 20px 0;
            font-family: 'Monaco', 'Cascadia Code', 'Roboto Mono', monospace;
            font-size: 0.9rem;
            overflow-x: auto;
            position: relative;
            border-left: 4px solid #667eea;
        }

        .code-header {
            background: #2a2a2a;
            color: #ccc;
            padding: 10px 20px;
            border-radius: 10px 10px 0 0;
            font-size: 0.8rem;
            border-left: 4px solid #667eea;
            margin: 20px 0 0 0;
        }

        .code-block + .code-block {
            margin-top: -20px;
            border-radius: 0 0 15px 15px;
        }

        /* Stats Grid */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .stat-card {
            background: linear-gradient(135deg, #667eea, #764ba2);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="40" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="2"/></svg>');
            opacity: 0.3;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 800;
            margin-bottom: 10px;
            position: relative;
            z-index: 2;
        }

        .stat-label {
            font-size: 1rem;
            opacity: 0.9;
            position: relative;
            z-index: 2;
        }

        /* Contributors */
        .contributors-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }

        .contributor {
            text-align: center;
            padding: 20px;
            border-radius: 15px;
            background: #f8f9ff;
            transition: all 0.3s ease;
        }

        .contributor:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .contributor-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea, #764ba2);
            margin: 0 auto 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 600;
            font-size: 1.2rem;
        }

        /* Footer */
        .footer {
            background: #1a1a1a;
            color: white;
            padding: 60px 0;
            text-align: center;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .footer-link {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .footer-link:hover {
            color: #667eea;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .section {
                padding: 40px 0;
            }
            
            .features-grid,
            .install-steps {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="logo">🚀</div>
                <h1>ProjectName</h1>
                <p>Modern, fast, and scalable application framework that empowers developers to build amazing experiences</p>
                
                <div class="badges">
                    <a href="#" class="badge">⭐ 2.3k Stars</a>
                    <a href="#" class="badge">🍴 450 Forks</a>
                    <a href="#" class="badge">📦 v2.1.0</a>
                    <a href="#" class="badge">✅ Build Passing</a>
                    <a href="#" class="badge">📄 MIT License</a>
                </div>

                <div class="cta-buttons">
                    <a href="#installation" class="btn btn-primary">
                        🚀 Get Started
                    </a>
                    <a href="#documentation" class="btn btn-secondary">
                        📖 Documentation
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Main Content -->
    <div class="main-content">
        <!-- Features Section -->
        <section class="section" id="features">
            <div class="container">
                <div class="section-header fade-in">
                    <h2>Powerful Features</h2>
                    <p>Everything you need to build modern applications, all in one package</p>
                </div>
                
                <div class="features-grid">
                    <div class="feature-card fade-in">
                        <div class="feature-icon">⚡</div>
                        <h3>Lightning Fast</h3>
                        <p>Optimized performance with sub-100ms response times and efficient resource usage</p>
                    </div>
                    
                    <div class="feature-card fade-in">
                        <div class="feature-icon">🔒</div>
                        <h3>Secure by Default</h3>
                        <p>Built-in security features including JWT authentication, rate limiting, and input validation</p>
                    </div>
                    
                    <div class="feature-card fade-in">
                        <div class="feature-icon">📱</div>
                        <h3>Mobile Ready</h3>
                        <p>Responsive design that works perfectly on all devices and screen sizes</p>
                    </div>
                    
                    <div class="feature-card fade-in">
                        <div class="feature-icon">🎨</div>
                        <h3>Highly Customizable</h3>
                        <p>Flexible theming system with support for custom components and layouts</p>
                    </div>
                    
                    <div class="feature-card fade-in">
                        <div class="feature-icon">🔄</div>
                        <h3>Real-time Updates</h3>
                        <p>WebSocket support for live data synchronization and instant notifications</p>
                    </div>
                    
                    <div class="feature-card fade-in">
                        <div class="feature-icon">🌐</div>
                        <h3>API First</h3>
                        <p>RESTful API with comprehensive documentation and SDK support</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Installation Section -->
        <section class="section" id="installation">
            <div class="container">
                <div class="section-header fade-in">
                    <h2>Quick Installation</h2>
                    <p>Get up and running in minutes with our simple installation process</p>
                </div>
                
                <div class="install-steps">
                    <div class="install-step fade-in">
                        <div class="step-number">1</div>
                        <h3>Install Package</h3>
                        <p>Use npm or yarn to install the package</p>
                    </div>
                    
                    <div class="install-step fade-in">
                        <div class="step-number">2</div>
                        <h3>Configure</h3>
                        <p>Set up your configuration file</p>
                    </div>
                    
                    <div class="install-step fade-in">
                        <div class="step-number">3</div>
                        <h3>Start Building</h3>
                        <p>Begin creating amazing applications</p>
                    </div>
                </div>

                <div class="fade-in">
                    <div class="code-header">Terminal</div>
                    <div class="code-block"># Install via npm
npm install project-name

# Or via yarn
yarn add project-name</div>
                </div>

                <div class="fade-in">
                    <div class="code-header">JavaScript</div>
                    <div class="code-block">import { ProjectName } from 'project-name';

// Initialize with configuration
const app = new ProjectName({
  apiKey: 'your-api-key',
  debug: true,
  theme: 'modern'
});

// Start your application
await app.initialize();
console.log('🎉 Application ready!');</div>
                </div>
            </div>
        </section>

        <!-- Stats Section -->
        <section class="section" id="stats">
            <div class="container">
                <div class="section-header fade-in">
                    <h2>Trusted by Developers</h2>
                    <p>Join thousands of developers building with ProjectName</p>
                </div>
                
                <div class="stats-grid">
                    <div class="stat-card fade-in">
                        <div class="stat-number">10k+</div>
                        <div class="stat-label">Active Users</div>
                    </div>
                    
                    <div class="stat-card fade-in">
                        <div class="stat-number">2.3k</div>
                        <div class="stat-label">GitHub Stars</div>
                    </div>
                    
                    <div class="stat-card fade-in">
                        <div class="stat-number">99.9%</div>
                        <div class="stat-label">Uptime</div>
                    </div>
                    
                    <div class="stat-card fade-in">
                        <div class="stat-number">50ms</div>
                        <div class="stat-label">Avg Response</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contributors Section -->
        <section class="section" id="contributors">
            <div class="container">
                <div class="section-header fade-in">
                    <h2>Amazing Contributors</h2>
                    <p>Thanks to all the wonderful people who made this project possible</p>
                </div>
                
                <div class="contributors-grid">
                    <div class="contributor fade-in">
                        <div class="contributor-avatar">JD</div>
                        <h4>John Doe</h4>
                        <p>Creator</p>
                    </div>
                    
                    <div class="contributor fade-in">
                        <div class="contributor-avatar">AS</div>
                        <h4>Alice Smith</h4>
                        <p>Core Developer</p>
                    </div>
                    
                    <div class="contributor fade-in">
                        <div class="contributor-avatar">BJ</div>
                        <h4>Bob Johnson</h4>
                        <p>UI/UX Designer</p>
                    </div>
                    
                    <div class="contributor fade-in">
                        <div class="contributor-avatar">CL</div>
                        <h4>Carol Lee</h4>
                        <p>Documentation</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-links">
                <a href="#" class="footer-link">📖 Documentation</a>
                <a href="#" class="footer-link">🐛 Issues</a>
                <a href="#" class="footer-link">💬 Discussions</a>
                <a href="#" class="footer-link">📧 Contact</a>
                <a href="#" class="footer-link">🐦 Twitter</a>
            </div>
            <p>&copy; 2025 ProjectName. Built with ❤️ by the community.</p>
        </div>
    </footer>

    <script>
        // Scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add some interactivity to feature cards
        document.querySelectorAll('.feature-card').forEach(card => {
            card.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-10px) scale(1.02)';
            });
            
            card.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(-10px) scale(1)';
            });
        });

        // Animated counter for stats
        function animateCounter(element, target, duration = 2000) {
            let start = 0;
            const increment = target / (duration / 16);
            
            function updateCounter() {
                start += increment;
                if (start < target) {
                    element.textContent = Math.floor(start).toLocaleString();
                    requestAnimationFrame(updateCounter);
                } else {
                    element.textContent = target.toLocaleString();
                }
            }
            
            updateCounter();
        }

        // Trigger counter animation when stats section is visible
        const statsObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const numbers = entry.target.querySelectorAll('.stat-number');
                    numbers.forEach(num => {
                        const text = num.textContent;
                        const value = parseInt(text.replace(/[^\d]/g, ''));
                        if (value && !num.dataset.animated) {
                            num.dataset.animated = 'true';
                            num.textContent = '0';
                            setTimeout(() => {
                                animateCounter(num, value);
                            }, 500);
                        }
                    });
                }
            });
        }, { threshold: 0.5 });

        const statsSection = document.getElementById('stats');
        if (statsSection) {
            statsObserver.observe(statsSection);
        }
    </script>
</body>
</html>
