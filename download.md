<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Download Joplin - Your Notes, Your Control</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Crimson+Pro:wght@400;600;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #1a5490;
            --primary-dark: #0d3a6b;
            --accent: #2196F3;
            --text: #1a1a1a;
            --text-light: #5a5a5a;
            --bg: #ffffff;
            --bg-secondary: #f8fafc;
            --border: #e2e8f0;
            --shadow: rgba(0, 0, 0, 0.08);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', -apple-system, sans-serif;
            line-height: 1.7;
            color: var(--text);
            background: var(--bg);
            -webkit-font-smoothing: antialiased;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #1a5490 0%, #0d3a6b 100%);
            color: white;
            text-align: center;
            padding: 4rem 2rem 3rem;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                radial-gradient(circle at 20% 50%, rgba(255,255,255,0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(255,255,255,0.05) 0%, transparent 50%);
            pointer-events: none;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
            animation: fadeInUp 0.8s ease-out;
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .logo {
            width: 160px;
            height: auto;
            margin-bottom: 1.5rem;
            filter: brightness(0) invert(1);
            animation: fadeIn 1s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .hero h1 {
            font-family: 'Crimson Pro', serif;
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 1rem;
            letter-spacing: -0.02em;
        }
        
        .hero-tagline {
            font-size: 1.25rem;
            opacity: 0.95;
            margin-bottom: 0.5rem;
        }
        
        .hero-subtitle {
            font-size: 1rem;
            opacity: 0.8;
        }
        
        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        /* Sections */
        section {
            padding: 4rem 0;
            animation: fadeInUp 0.6s ease-out;
        }
        
        section:nth-child(even) {
            background: var(--bg-secondary);
        }
        
        h2 {
            font-family: 'Crimson Pro', serif;
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 2rem;
            color: var(--primary-dark);
            letter-spacing: -0.01em;
        }
        
        h3 {
            font-family: 'Crimson Pro', serif;
            font-size: 1.75rem;
            font-weight: 600;
            margin: 2rem 0 1rem;
            color: var(--text);
        }
        
        /* Platform Cards */
        .platform-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }
        
        .platform-card {
            background: white;
            border-radius: 12px;
            padding: 2rem;
            box-shadow: 0 4px 12px var(--shadow);
            transition: all 0.3s ease;
            border: 1px solid var(--border);
        }
        
        .platform-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 8px 24px var(--shadow);
        }
        
        .download-badge {
            display: inline-block;
            margin: 1rem 0;
            transition: transform 0.2s ease;
        }
        
        .download-badge:hover {
            transform: scale(1.05);
        }
        
        .download-badge img {
            width: 140px;
            height: auto;
        }
        
        .requirements {
            background: var(--bg-secondary);
            border-left: 3px solid var(--accent);
            padding: 1rem 1.5rem;
            margin: 1rem 0;
            border-radius: 4px;
            font-size: 0.9rem;
            color: var(--text-light);
        }
        
        .requirements strong {
            color: var(--text);
        }
        
        /* Feature List */
        .feature-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        .feature-item {
            display: flex;
            align-items: flex-start;
            gap: 0.75rem;
        }
        
        .feature-item::before {
            content: '✦';
            color: var(--accent);
            font-size: 1.2rem;
            flex-shrink: 0;
        }
        
        /* Code Blocks */
        pre {
            background: #1e293b;
            color: #e2e8f0;
            padding: 1.5rem;
            border-radius: 8px;
            overflow-x: auto;
            margin: 1.5rem 0;
            font-family: 'Monaco', 'Courier New', monospace;
            font-size: 0.9rem;
            line-height: 1.6;
        }
        
        code {
            background: var(--bg-secondary);
            padding: 0.2rem 0.5rem;
            border-radius: 4px;
            font-family: 'Monaco', 'Courier New', monospace;
            font-size: 0.9rem;
        }
        
        /* Links */
        a {
            color: var(--accent);
            text-decoration: none;
            transition: color 0.2s ease;
        }
        
        a:hover {
            color: var(--primary);
            text-decoration: underline;
        }
        
        /* Blockquote */
        blockquote {
            border-left: 4px solid var(--accent);
            padding: 1.5rem 2rem;
            margin: 2rem 0;
            background: var(--bg-secondary);
            font-family: 'Crimson Pro', serif;
            font-size: 1.25rem;
            font-style: italic;
            color: var(--text);
        }
        
        /* Lists */
        ul {
            margin: 1rem 0;
            padding-left: 2rem;
        }
        
        li {
            margin: 0.5rem 0;
        }
        
        /* Sync Options */
        .sync-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        .sync-option {
            background: white;
            padding: 1.5rem;
            border-radius: 8px;
            border: 2px solid var(--border);
            transition: all 0.3s ease;
        }
        
        .sync-option:hover {
            border-color: var(--accent);
            transform: translateY(-2px);
        }
        
        .sync-option strong {
            display: block;
            color: var(--primary);
            margin-bottom: 0.5rem;
            font-size: 1.1rem;
        }
        
        /* Call to Action */
        .cta-box {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            color: white;
            padding: 3rem;
            border-radius: 12px;
            text-align: center;
            margin: 3rem 0;
        }
        
        .cta-box h3 {
            color: white;
            margin-bottom: 1rem;
        }
        
        .cta-links {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            margin-top: 1.5rem;
            flex-wrap: wrap;
        }
        
        .cta-link {
            background: rgba(255,255,255,0.2);
            color: white;
            padding: 0.75rem 1.5rem;
            border-radius: 6px;
            text-decoration: none;
            transition: all 0.3s ease;
            border: 1px solid rgba(255,255,255,0.3);
        }
        
        .cta-link:hover {
            background: rgba(255,255,255,0.3);
            transform: translateY(-2px);
            text-decoration: none;
        }
        
        /* Footer */
        footer {
            text-align: center;
            padding: 3rem 2rem;
            background: var(--bg-secondary);
            color: var(--text-light);
            font-size: 0.9rem;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 2rem;
            }
            
            .platform-grid,
            .feature-list,
            .sync-grid {
                grid-template-columns: 1fr;
            }
            
            section {
                padding: 3rem 0;
            }
        }
        
        /* Smooth scroll */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <div class="hero">
        <div class="hero-content">
            <img src="https://joplinapp.org/images/logo-text.svg" alt="Joplin" class="logo">
            <h1>Download Joplin</h1>
            <p class="hero-tagline"><strong>Notes, without compromise.</strong></p>
            <p class="hero-subtitle">Private by design • Offline-first • Yours forever</p>
        </div>
    </div>

    <!-- Desktop Apps -->
    <section>
        <div class="container">
            <h2>Desktop Applications</h2>
            <p>Access your notes on Windows, macOS, or Linux.</p>
            
            <div class="platform-grid">
                <div class="platform-card">
                    <h3>Windows</h3>
                    <a href="https://objects.joplinusercontent.com/v3.5.13/Joplin-Setup-3.5.13.exe?source=JoplinWebsite&type=New" class="download-badge">
                        <img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeWindows.png" alt="Get it on Windows">
                    </a>
                    <div class="requirements">
                        <strong>System Requirements:</strong><br>
                        • Windows 10 or later<br>
                        • 200 MB free disk space
                    </div>
                </div>

                <div class="platform-card">
                    <h3>macOS</h3>
                    <a href="https://objects.joplinusercontent.com/v3.5.13/Joplin-3.5.13.dmg?source=JoplinWebsite&type=New" class="download-badge">
                        <img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeMacOS.png" alt="Get it on macOS">
                    </a>
                    <p style="margin: 1rem 0;"><strong>Apple Silicon (M1/M2/M3):</strong></p>
                    <a href="https://objects.joplinusercontent.com/v3.5.13/Joplin-3.5.13-arm64.DMG?source=JoplinWebsite&type=New" class="download-badge">
                        <img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeMacOSM1.png" alt="Get it on macOS M1">
                    </a>
                    <div class="requirements">
                        <strong>System Requirements:</strong><br>
                        • macOS 10.13 or later<br>
                        • 200 MB free disk space
                    </div>
                </div>

                <div class="platform-card">
                    <h3>Linux</h3>
                    <a href="https://objects.joplinusercontent.com/v3.5.13/Joplin-3.5.13.AppImage?source=JoplinWebsite&type=New" class="download-badge">
                        <img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeLinux.png" alt="Get it on Linux">
                    </a>
                    <div class="requirements">
                        <strong>Alternative Methods:</strong><br>
                        • Flatpak: <code>flatpak install flathub net.cozic.joplin_desktop</code><br>
                        • Snap: <code>sudo snap install joplin-desktop</code><br>
                        • AUR: <code>yay -S joplin-appimage</code>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Mobile Apps -->
    <section>
        <div class="container">
            <h2>Mobile Applications</h2>
            <p>Take your notes anywhere with native mobile apps.</p>
            
            <div class="platform-grid">
                <div class="platform-card">
                    <h3>Android</h3>
                    <a href="https://play.google.com/store/apps/details?id=net.cozic.joplin" class="download-badge">
                        <img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeAndroid.png" alt="Get it on Google Play" style="width: 160px;">
                    </a>
                    <p style="margin-top: 1rem;"><strong>Alternative:</strong> <a href="https://github.com/laurent22/joplin/releases">Download APK directly</a></p>
                    <div class="requirements">
                        <strong>Requirements:</strong> Android 5.0 or later
                    </div>
                </div>

                <div class="platform-card">
                    <h3>iOS</h3>
                    <a href="https://itunes.apple.com/us/app/joplin/id1315599797" class="download-badge">
                        <img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeIOS.png" alt="Download on App Store" style="width: 160px;">
                    </a>
                    <div class="requirements">
                        <strong>Requirements:</strong> iOS 13.0 or later
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Terminal & Web Clipper -->
    <section>
        <div class="container">
            <h2>Additional Tools</h2>
            
            <h3>Terminal Application</h3>
            <p>For command-line enthusiasts and server deployments.</p>
            <pre># Install via npm
npm install -g joplin

# Run Joplin
joplin</pre>
            <p><strong>Requirements:</strong> Node.js 18 or later • <a href="https://joplinapp.org/help/apps/terminal/">View CLI documentation →</a></p>

            <h3 style="margin-top: 3rem;">Web Clipper</h3>
            <p>Save web pages directly to Joplin from your browser.</p>
            <div style="margin: 1.5rem 0;">
                <a href="https://chrome.google.com/webstore/detail/joplin-web-clipper/alofnhikmmkdbbbgpnglcpdollgjjfek">Chrome Web Store</a> • 
                <a href="https://addons.mozilla.org/en-US/firefox/addon/joplin-web-clipper/">Firefox Add-ons</a>
            </div>
        </div>
    </section>

    <!-- Synchronization -->
    <section>
        <div class="container">
            <h2>Synchronization</h2>
            <p>Keep your notes in sync across all devices.</p>

            <div class="cta-box">
                <h3>Joplin Cloud (Recommended)</h3>
                <p>Officially supported cloud service with end-to-end encryption, automatic backups, and note sharing.</p>
                <p><strong>10 GB storage free tier</strong></p>
                <div style="margin-top: 1.5rem;">
                    <a href="https://joplinapp.org/plans/" class="cta-link">Get Joplin Cloud →</a>
                </div>
            </div>

            <h3>Self-Hosted Options</h3>
            <div class="sync-grid">
                <div class="sync-option">
                    <strong>Dropbox</strong>
                    Simple setup, widely used
                </div>
                <div class="sync-option">
                    <strong>OneDrive</strong>
                    Microsoft integration
                </div>
                <div class="sync-option">
                    <strong>Nextcloud</strong>
                    Self-hosted control
                </div>
                <div class="sync-option">
                    <strong>WebDAV</strong>
                    Universal protocol
                </div>
                <div class="sync-option">
                    <strong>S3</strong>
                    Amazon Web Services
                </div>
                <div class="sync-option">
                    <strong>Joplin Server</strong>
                    Self-host your own sync
                </div>
            </div>
            <p style="margin-top: 1.5rem;"><a href="https://joplinapp.org/help/apps/sync/">View sync setup guide →</a></p>
        </div>
    </section>

    <!-- Why Joplin -->
    <section>
        <div class="container">
            <h2>Why Choose Joplin?</h2>
            
            <blockquote>
                Your notes belong to you.
            </blockquote>

            <h3>✦ Your Data, Your Control</h3>
            <ul>
                <li><strong>No lock-in:</strong> Open format, export anytime</li>
                <li><strong>No forced cloud:</strong> Sync only if you want</li>
                <li><strong>No compromises:</strong> Full-featured, always free</li>
            </ul>

            <h3>✦ Core Features</h3>
            <div class="feature-list">
                <div class="feature-item">
                    <div><strong>Markdown editor</strong> with live preview</div>
                </div>
                <div class="feature-item">
                    <div><strong>End-to-end encryption</strong> for security</div>
                </div>
                <div class="feature-item">
                    <div><strong>Cross-platform sync</strong> across all devices</div>
                </div>
                <div class="feature-item">
                    <div><strong>Offline-first</strong> - works without internet</div>
                </div>
                <div class="feature-item">
                    <div><strong>Open data format</strong> - never trapped</div>
                </div>
                <div class="feature-item">
                    <div><strong>Plugin system</strong> - extend functionality</div>
                </div>
                <div class="feature-item">
                    <div><strong>Attachments</strong> - images, PDFs, files</div>
                </div>
                <div class="feature-item">
                    <div><strong>Tags and notebooks</strong> - organize your way</div>
                </div>
                <div class="feature-item">
                    <div><strong>Full-text search</strong> - find anything instantly</div>
                </div>
            </div>

            <h3>✦ Philosophy</h3>
            <p>Joplin is built on principles of:</p>
            <ul>
                <li><strong>Portability</strong> - Take your data anywhere</li>
                <li><strong>Durability</strong> - Notes that last forever</li>
                <li><strong>Independence</strong> - No service dependencies</li>
            </ul>
        </div>
    </section>

    <!-- Support -->
    <section>
        <div class="container">
            <h2>Support the Project</h2>
            <p>Joplin is free and open source. Support development:</p>
            <div class="cta-links" style="justify-content: flex-start; margin-top: 1.5rem;">
                <a href="https://github.com/sponsors/laurent22" class="cta-link">💙 GitHub Sponsors</a>
                <a href="https://www.paypal.com/donate/?business=E8JMYD2LQ8MMA" class="cta-link">☕ PayPal</a>
                <a href="https://www.patreon.com/joplin" class="cta-link">🎁 Patreon</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p><strong>Additional Resources</strong></p>
            <p style="margin: 1rem 0;">
                <a href="https://joplinapp.org/help/">Documentation</a> • 
                <a href="https://discourse.joplinapp.org/">Community Forum</a> • 
                <a href="https://github.com/laurent22/joplin/issues">Report Issues</a> • 
                <a href="https://twitter.com/joplinapp">Twitter</a>
            </p>
            <p style="margin-top: 2rem; opacity: 0.7;">
                <em>Minimal • Local-first • Durable</em>
            </p>
            <p style="margin-top: 1rem; font-size: 0.85rem; opacity: 0.6;">
                Current Version: 3.5.13
            </p>
        </div>
    </footer>

    <script>
        // Smooth scroll animation observer
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        document.querySelectorAll('section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(30px)';
            section.style.transition = 'opacity 0.6s ease-out, transform 0.6s ease-out';
            observer.observe(section);
        });
    </script>
</body>
</html>
