/* ========================================
   NATARAJA M - PROFESSIONAL PORTFOLIO CSS
   ======================================== */

/* ========== GLOBAL STYLES ========== */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Poppins', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 100%);
    color: #fff;
    overflow-x: hidden;
    line-height: 1.6;
}

/* ========== CUSTOM SCROLLBAR ========== */
::-webkit-scrollbar {
    width: 10px;
}

::-webkit-scrollbar-track {
    background: #1a1a2e;
}

::-webkit-scrollbar-thumb {
    background: linear-gradient(135deg, #667eea, #764ba2);
    border-radius: 10px;
}

::-webkit-scrollbar-thumb:hover {
    background: linear-gradient(135deg, #764ba2, #667eea);
}

/* ========== TYPOGRAPHY ========== */
h1, h2, h3, h4, h5, h6 {
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 1rem;
}

h1 {
    font-size: clamp(2.5rem, 5vw, 4rem);
    background: linear-gradient(135deg, #fff, #667eea, #764ba2);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

h2 {
    font-size: clamp(2rem, 4vw, 3rem);
    color: #667eea;
}

.section-title {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 3rem;
    position: relative;
}

.section-title::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    width: 80px;
    height: 3px;
    background: linear-gradient(90deg, #667eea, #764ba2);
    border-radius: 2px;
}

/* ========== CONTAINER ========== */
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* ========== NAVIGATION ========== */
nav {
    position: fixed;
    top: 0;
    width: 100%;
    background: rgba(10, 10, 10, 0.95);
    backdrop-filter: blur(10px);
    z-index: 1000;
    padding: 1rem 0;
    transition: all 0.3s ease;
    border-bottom: 1px solid rgba(102,126,234,0.2);
}

nav.scrolled {
    padding: 0.5rem 0;
    background: rgba(10, 10, 10, 0.98);
    box-shadow: 0 2px 20px rgba(0,0,0,0.3);
}

nav .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-size: 1.8rem;
    font-weight: 800;
    background: linear-gradient(135deg, #667eea, #764ba2);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}

.nav-links {
    display: flex;
    list-style: none;
    gap: 2rem;
}

.nav-links a {
    color: #fff;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s;
    position: relative;
}

.nav-links a::before {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 0;
    height: 2px;
    background: linear-gradient(90deg, #667eea, #764ba2);
    transition: width 0.3s;
}

.nav-links a:hover::before {
    width: 100%;
}

/* ========== BUTTONS ========== */
.btn {
    display: inline-block;
    padding: 12px 30px;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s;
    border: none;
    cursor: pointer;
}

.btn-primary {
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: #fff;
    box-shadow: 0 4px 15px rgba(102,126,234,0.3);
}

.btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 20px rgba(102,126,234,0.4);
}

.btn-outline {
    background: transparent;
    border: 2px solid #667eea;
    color: #fff;
}

.btn-outline:hover {
    background: rgba(102,126,234,0.1);
    transform: translateY(-3px);
}

/* ========== HERO SECTION ========== */
.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    text-align: center;
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
    background: radial-gradient(circle at 50% 50%, rgba(102,126,234,0.1), transparent);
    z-index: -1;
}

.hero-content {
    animation: fadeInUp 0.8s ease;
}

.hero h1 {
    font-size: clamp(2rem, 5vw, 4rem);
    margin-bottom: 1rem;
}

.hero .highlight {
    color: #667eea;
}

.hero h2 {
    font-size: clamp(1.2rem, 3vw, 2rem);
    color: #aaa;
    margin-bottom: 1rem;
}

.hero p {
    max-width: 600px;
    margin: 0 auto 2rem;
    color: #aaa;
}

/* ========== SECTIONS ========== */
section {
    padding: 5rem 0;
}

/* ========== PROJECTS GRID ========== */
.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 2rem;
}

.project-card {
    background: rgba(255,255,255,0.05);
    backdrop-filter: blur(10px);
    border-radius: 20px;
    overflow: hidden;
    transition: all 0.3s;
    border: 1px solid rgba(255,255,255,0.1);
}

.project-card:hover {
    transform: translateY(-10px);
    border-color: rgba(102,126,234,0.5);
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
}

.project-image {
    height: 200px;
    background: linear-gradient(135deg, #667eea, #764ba2);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 4rem;
    color: #fff;
}

.project-card h3 {
    padding: 1.5rem 1.5rem 0.5rem;
}

.project-card p {
    padding: 0 1.5rem;
    color: #aaa;
}

.tech-tags {
    padding: 1rem 1.5rem;
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
}

.tech-tags span {
    background: rgba(102,126,234,0.2);
    padding: 0.3rem 0.8rem;
    border-radius: 20px;
    font-size: 0.75rem;
    color: #667eea;
}

.project-links {
    padding: 0 1.5rem 1.5rem;
    display: flex;
    gap: 1.5rem;
}

.project-links a {
    color: #667eea;
    text-decoration: none;
    transition: color 0.3s;
}

.project-links a:hover {
    color: #764ba2;
}

/* ========== SKILLS GRID ========== */
.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
    gap: 1.5rem;
}

.skill-card {
    text-align: center;
    padding: 1.5rem;
    background: rgba(255,255,255,0.05);
    border-radius: 15px;
    backdrop-filter: blur(10px);
    transition: all 0.3s;
    cursor: pointer;
}

.skill-card i {
    font-size: 3rem;
    margin-bottom: 0.5rem;
    background: linear-gradient(135deg, #667eea, #764ba2);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.skill-card span {
    display: block;
    font-size: 0.9rem;
}

.skill-card:hover {
    transform: translateY(-5px);
    background: linear-gradient(135deg, #667eea, #764ba2);
}

.skill-card:hover i {
    -webkit-text-fill-color: white;
}

.skill-card:hover span {
    color: white;
}

/* ========== TIMELINE ========== */
.timeline {
    max-width: 800px;
    margin: 0 auto;
    position: relative;
}

.timeline::before {
    content: '';
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    width: 2px;
    height: 100%;
    background: linear-gradient(180deg, #667eea, #764ba2);
}

.timeline-item {
    margin-bottom: 3rem;
    position: relative;
}

.timeline-content {
    width: 45%;
    padding: 1.5rem;
    background: rgba(255,255,255,0.05);
    border-radius: 15px;
    backdrop-filter: blur(10px);
    position: relative;
}

.timeline-item:nth-child(odd) .timeline-content {
    margin-left: 55%;
}

.timeline-item:nth-child(even) .timeline-content {
    margin-right: 55%;
    text-align: right;
}

.timeline-date {
    color: #667eea;
    font-weight: 600;
    margin-bottom: 0.5rem;
}

/* ========== STATS SECTION ========== */
.stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 2rem;
    text-align: center;
}

.stat-card {
    padding: 2rem;
    background: rgba(255,255,255,0.03);
    border-radius: 20px;
    backdrop-filter: blur(10px);
    transition: all 0.3s;
}

.stat-card:hover {
    transform: translateY(-5px);
    background: rgba(102,126,234,0.1);
}

.stat-number {
    font-size: 3rem;
    font-weight: 800;
    background: linear-gradient(135deg, #667eea, #764ba2);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

/* ========== CONTACT SECTION ========== */
.contact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
}

.contact-card {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1.5rem;
    background: rgba(255,255,255,0.05);
    border-radius: 15px;
    backdrop-filter: blur(10px);
    text-decoration: none;
    color: #fff;
    transition: all 0.3s;
}

.contact-card:hover {
    transform: translateX(10px);
    background: rgba(102,126,234,0.1);
}

.contact-icon {
    width: 50px;
    height: 50px;
    background: linear-gradient(135deg, #667eea, #764ba2);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
}

/* ========== FORM STYLES ========== */
.form-group {
    margin-bottom: 1.5rem;
}

.form-group input,
.form-group textarea {
    width: 100%;
    padding: 1rem;
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 10px;
    color: #fff;
    font-family: inherit;
    transition: all 0.3s;
}

.form-group input:focus,
.form-group textarea:focus {
    outline: none;
    border-color: #667eea;
}

/* ========== FOOTER ========== */
footer {
    background: linear-gradient(135deg, rgba(102,126,234,0.1), rgba(118,75,162,0.1));
    text-align: center;
    padding: 2rem 0;
    margin-top: 2rem;
}

/* ========== ANIMATIONS ========== */
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

@keyframes fadeInRight {
    from {
        opacity: 0;
        transform: translateX(30px);
    }
    to {
        opacity: 1;
        transform: translateX(0);
    }
}

/* ========== RESPONSIVE DESIGN ========== */
@media (max-width: 768px) {
    .nav-links {
        display: none;
    }
    
    .timeline::before {
        left: 20px;
    }
    
    .timeline-content {
        width: calc(100% - 50px);
        margin-left: 50px !important;
        text-align: left !important;
    }
    
    .projects-grid {
        grid-template-columns: 1fr;
    }
    
    .skills-grid {
        grid-template-columns: repeat(2, 1fr);
    }
    
    .stats-grid {
        grid-template-columns: repeat(2, 1fr);
    }
    
    .hero h1 {
        font-size: 2rem;
    }
}

/* ========== LOADING ANIMATION ========== */
.loader {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #0a0a0a;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 9999;
    transition: opacity 0.5s;
}

.loader.hide {
    opacity: 0;
    pointer-events: none;
}

.spinner {
    width: 50px;
    height: 50px;
    border: 3px solid rgba(102,126,234,0.3);
    border-top-color: #667eea;
    border-radius: 50%;
    animation: spin 1s linear infinite;
}

@keyframes spin {
    to { transform: rotate(360deg); }
}

/* ========== SCROLL TO TOP BUTTON ========== */
.scroll-top {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 50px;
    height: 50px;
    background: linear-gradient(135deg, #667eea, #764ba2);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    cursor: pointer;
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s;
    z-index: 999;
}

.scroll-top.show {
    opacity: 1;
    visibility: visible;
}

.scroll-top:hover {
    transform: translateY(-5px);
}

/* ========== DARK MODE TOGGLE ========== */
.dark-mode-btn {
    background: #333;
    border: none;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    cursor: pointer;
    font-size: 1.2rem;
    transition: all 0.3s;
}

.dark-mode-btn:hover {
    transform: scale(1.1);
}

/* ========== PARTICLE BACKGROUND ========== */
#particles-bg {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -2;
    pointer-events: none;
}
### 👋 Hi, I'm Nataraja M

**Python Developer | Backend Architect**

📍 Hospet, Karnataka, India  
🎓 BCA at Vijayanagara Sri Krishnadevaraya University (CGPA: 8.9/10)  
📧 nataraja7892@gmail.com  

---

### 🚀 About Me

- 🔭 I build scalable backend systems and REST APIs
- 🌱 Learning System Design & Cloud Architecture
- 💬 Ask me about Python, Django, FastAPI
- ⚡ Fun fact: Code. Learn. Build. Repeat.

---

### 📊 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=nataraja7892-lab&show_icons=true&theme=dark)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=nataraja7892-lab&layout=compact&theme=dark)

---

### 💻 Tech Stack

- **Languages:** Python, JavaScript, SQL, C++
- **Frameworks:** Django, FastAPI, React, Node.js
- **Databases:** PostgreSQL, MySQL, MongoDB, SQLite
- **Tools:** Docker, Git, Redis, AWS

---

### 📈 LeetCode

![LeetCode Stats](https://leetcard.jacoblin.cool/Natarajam1234?theme=dark)

- Easy: 103 | Medium: 106 | Hard: 21 | Total: 230+

---

### 🎯 Featured Projects

- **Employee Management System** - [Live Demo](https://employee-management-1-1a5p.onrender.com) | [GitHub](https://github.com/nataraja7892-lab/employee-management)
- **Exam Management Platform** - [Live Demo](https://exam-managements-6.onrender.com) | [GitHub](https://github.com/nataraja7892-lab/exam_managements)

---

### 📫 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nataraja-m-707622384/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nataraja7892-lab)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:nataraja7892@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=google-chrome&logoColor=white)](https://graceful-travesseiro-a51e31.netlify.app/)

---

### 🎨 Visitor Counter

![Visitors](https://komarev.com/ghpvc/?username=nataraja7892-lab&color=blue)

---

**Thanks for visiting! Have a great day!** 🚀
