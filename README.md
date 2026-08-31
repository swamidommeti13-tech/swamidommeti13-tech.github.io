/* --- Global Resets & Variables --- */
:root {
  --bg-dark: #0f172a;
  --bg-card: #1e293b;
  --accent-blue: #3b82f6;
  --accent-cyan: #06b6d4;
  --text-main: #f8fafc;
  --text-muted: #94a3b8;
  --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
  font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
  background-color: var(--bg-dark);
  color: var(--text-main);
}

body {
  line-height: 1.6;
}

/* --- Top Navigation --- */
.top-nav {
  position: sticky;
  top: 0;
  z-index: 100;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.25rem 10%;
  background: rgba(15, 23, 42, 0.85);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.top-nav .logo {
  font-size: 1.5rem;
  font-weight: 700;
  background: linear-gradient(135deg, var(--accent-blue), var(--accent-cyan));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.top-nav nav a {
  color: var(--text-muted);
  text-decoration: none;
  margin-left: 2rem;
  font-weight: 500;
  transition: var(--transition);
}

.top-nav nav a:hover {
  color: var(--accent-cyan);
}

/* --- Hero Section & Animations --- */
.hero {
  min-height: 85vh;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 10%;
  gap: 2rem;
  background: radial-gradient(circle at top right, rgba(6, 182, 212, 0.15), transparent 50%);
  animation: fadeIn 1s ease-in;
}

.hero-content {
  max-width: 600px;
}

.tagline {
  display: inline-block;
  color: var(--accent-cyan);
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-size: 0.875rem;
  margin-bottom: 1rem;
}

.hero h1 {
  font-size: 3.25rem;
  line-height: 1.1;
  margin-bottom: 1rem;
}

.subtitle {
  color: var(--text-muted);
  font-size: 1.15rem;
  margin-bottom: 2rem;
}

.hero-actions {
  display: flex;
  gap: 1rem;
}

.btn {
  padding: 0.8rem 1.75rem;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  transition: var(--transition);
}

.btn.primary {
  background: linear-gradient(135deg, var(--accent-blue), var(--accent-cyan));
  color: #fff;
  box-shadow: 0 4px 15px rgba(6, 182, 212, 0.3);
}

.btn.primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(6, 182, 212, 0.5);
}

.btn.secondary {
  border: 1px solid var(--text-muted);
  color: var(--text-main);
}

.btn.secondary:hover {
  background: rgba(255, 255, 255, 0.05);
  border-color: var(--accent-cyan);
  color: var(--accent-cyan);
}

.hero-photo img {
  width: 280px;
  height: 280px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid var(--accent-blue);
  box-shadow: 0 0 25px rgba(59, 130, 246, 0.4);
  animation: pulse 4s infinite ease-in-out;
}

/* --- Content Sections --- */
.section {
  padding: 5rem 10%;
}

.section h2 {
  font-size: 2.25rem;
  margin-bottom: 1.5rem;
  position: relative;
}

.section h2::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -6px;
  width: 50px;
  height: 4px;
  background: var(--accent-cyan);
  border-radius: 2px;
}

.section p {
  color: var(--text-muted);
  font-size: 1.1rem;
  margin-bottom: 1rem;
  max-width: 800px;
}

/* --- Skills Pills --- */
.pill-list {
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
  list-style: none;
  margin-top: 1.5rem;
}

.pill-list li {
  background: var(--bg-card);
  padding: 0.6rem 1.25rem;
  border-radius: 20px;
  border: 1px solid rgba(255, 255, 255, 0.05);
  color: var(--accent-cyan);
  font-weight: 500;
  transition: var(--transition);
}

.pill-list li:hover {
  transform: translateY(-4px);
  background: var(--accent-blue);
  color: #fff;
}

/* --- Project Cards Grid --- */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}

.project-card {
  background: var(--bg-card);
  padding: 2rem;
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.05);
  transition: var(--transition);
}

.project-card:hover {
  transform: translateY(-8px);
  border-color: var(--accent-blue);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
}

.project-card h3 {
  font-size: 1.4rem;
  margin-bottom: 0.75rem;
}

.project-card p {
  font-size: 0.95rem;
  margin-bottom: 1.5rem;
}

.project-card a {
  color: var(--accent-cyan);
  text-decoration: none;
  font-weight: 600;
  transition: var(--transition);
}

.project-card a:hover {
  color: var(--accent-blue);
}

/* --- Contact & Footer --- */
#contact a {
  color: var(--accent-cyan);
  text-decoration: none;
}

.footer {
  text-align: center;
  padding: 2rem;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  color: var(--text-muted);
  font-size: 0.9rem;
}

/* --- Keyframe Animations --- */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes pulse {
  0%, 100% { transform: scale(1); box-shadow: 0 0 25px rgba(59, 130, 246, 0.4); }
  50% { transform: scale(1.03); box-shadow: 0 0 35px rgba(6, 182, 212, 0.6); }
}

/* --- Mobile Responsiveness --- */
@media (max-width: 768px) {
  .hero {
    flex-direction: column-reverse;
    text-align: center;
    padding-top: 3rem;
  }
  .hero-actions {
    justify-content: center;
  }
  .section h2::after {
    left: 50%;
    transform: translateX(-50%);
  }
  .section {
    text-align: center;
  }
}
