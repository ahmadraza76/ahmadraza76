import React from 'react';

export default function App() {
  return (
    <div className="bg-gray-100 min-h-screen font-sans text-gray-800">
      {/* Header */}
      <header className="bg-gradient-to-r from-gray-900 to-black text-white py-16 px-4 text-center">
        <img
          src="https://github.com/ahmadraza76/ahmadraza76/blob/main/IMG_20240510_194118.jpg?raw=true "
          alt="Ahmad Raza Profile"
          className="w-32 h-32 rounded-full border-4 border-white shadow-lg mx-auto mb-6 transition-transform duration-300 hover:scale-110"
        />
        <h1 className="text-4xl md:text-5xl font-bold mb-4">👋 Hi, I'm Ahmad Raza!</h1>
        <p className="text-xl md:text-2xl max-w-3xl mx-auto">
          Welcome to my GitHub universe! I'm a passionate developer, open-source advocate, and a creative coder who loves transforming ideas into reality. Let's build something extraordinary together! 🚀
        </p>
      </header>

      {/* About Section */}
      <section className="py-12 px-6 bg-white">
        <div className="max-w-4xl mx-auto">
          <h2 className="text-3xl font-bold mb-6 flex items-center">
            <span className="mr-2">🌟</span> About Me
          </h2>
          <ul className="list-disc pl-6 space-y-2">
            <li><strong>💻 Specialization:</strong> Full-Stack Development with a focus on crafting intuitive and scalable web applications.</li>
            <li><strong>🌱 Currently Learning:</strong> Advanced AI/ML frameworks, Web3, and micro-interaction animations.</li>
            <li><strong>🔥 Passionate About:</strong> Open-source contributions, pixel-perfect UI/UX, and creating delightful user experiences.</li>
            <li><strong>🎨 Hobbies:</strong> Experimenting with SVG animations, designing futuristic interfaces, and exploring new tech trends.</li>
          </ul>
        </div>
      </section>

      {/* Technologies Section */}
      <section className="py-12 px-6 bg-gray-50">
        <div className="max-w-5xl mx-auto">
          <h2 className="text-3xl font-bold mb-6 text-center">🛠️ Technologies & Tools</h2>
          <p className="text-center mb-6">A collection of my favorite tools and languages, brought to life with animated SVG badges!</p>
          <div className="flex justify-center flex-wrap gap-4">
            {[
              { name: "JavaScript", src: "https://img.shields.io/badge/JavaScript-%23F7DF1E?style=for-the-badge&logo=javascript&logoColor=black " },
              { name: "Python", src: "https://img.shields.io/badge/Python-%233776AB?style=for-the-badge&logo=python&logoColor=white " },
              { name: "Node.js", src: "https://img.shields.io/badge/Node.js-%23339933?style=for-the-badge&logo=node.js&logoColor=white " },
              { name: "React", src: "https://img.shields.io/badge/React-%2361DAFB?style=for-the-badge&logo=react&logoColor=black " },
              { name: "Tailwind CSS", src: "https://img.shields.io/badge/Tailwind_CSS-%2306B6D4?style=for-the-badge&logo=tailwind-css&logoColor=white " }
            ].map((badge, index) => (
              <a key={index} href="#" target="_blank" rel="noopener noreferrer">
                <img
                  src={badge.src}
                  alt={badge.name}
                  className="badge-img"
                  style={{
                    transition: 'transform 0.3s ease-in-out',
                    cursor: 'pointer'
                  }}
                  onMouseOver={(e) => e.currentTarget.style.transform = 'scale(1.1)'}
                  onMouseOut={(e) => e.currentTarget.style.transform = 'scale(1)'}
                />
              </a>
            ))}
          </div>
        </div>
      </section>

      {/* GitHub Stats */}
      <section className="py-12 px-6 bg-white">
        <div className="max-w-5xl mx-auto">
          <h2 className="text-3xl font-bold mb-6 text-center">📊 GitHub Stats</h2>
          <p className="text-center mb-6">Track my coding journey with these sleek, animated stats!</p>
          <div className="flex flex-col md:flex-row justify-center gap-6">
            <img
              src="https://github-readme-stats.vercel.app/api?username=ahmadraza76&show_icons=true&theme=dracula&hide_border=true&count_private=true "
              alt="GitHub Stats"
              className="rounded-lg shadow-md transition-transform duration-300 hover:scale-105"
            />
            <img
              src="https://github-readme-streak-stats.herokuapp.com/?user=ahmadraza76&theme=dracula&hide_border=true "
              alt="GitHub Streak"
              className="rounded-lg shadow-md transition-transform duration-300 hover:scale-105"
            />
          </div>
        </div>
      </section>

      {/* Projects */}
      <section className="py-12 px-6 bg-gray-50">
        <div className="max-w-4xl mx-auto">
          <h2 className="text-3xl font-bold mb-6">✨ Featured Projects</h2>
          <div className="space-y-8">
            <div className="bg-white p-6 rounded-lg shadow hover:shadow-xl transition-shadow">
              <h3 className="text-xl font-semibold mb-2">🚀 Project Name</h3>
              <p>A responsive portfolio site with animated SVGs.</p>
              <p className="mt-2"><strong>Tech Stack:</strong> React, Tailwind CSS, Lottie Animations</p>
              <div className="mt-3 flex gap-2">
                <a href="#!" className="text-blue-600 underline">Live Demo</a>
                <a href="#!" className="text-blue-600 underline">Repo</a>
              </div>
              <img
                src="https://img.icons8.com/?size=100&id=108639&format=png&color=000000 "
                alt="Project Icon"
                className="w-10 mt-3 transition-transform duration-300 hover:rotate-360"
                style={{ transition: 'transform 0.3s ease' }}
              />
            </div>

            <div className="bg-white p-6 rounded-lg shadow hover:shadow-xl transition-shadow">
              <h3 className="text-xl font-semibold mb-2">🌐 Real-Time Chat App</h3>
              <p>A real-time chat app with micro-interactions.</p>
              <p className="mt-2"><strong>Tech Stack:</strong> Node.js, Socket.io, Framer Motion</p>
              <div className="mt-3 flex gap-2">
                <a href="#!" className="text-blue-600 underline">Live Demo</a>
                <a href="#!" className="text-blue-600 underline">Repo</a>
              </div>
              <img
                src="https://img.icons8.com/?size=100&id=108784&format=png&color=000000 "
                alt="Project Icon"
                className="w-10 mt-3 transition-transform duration-300 hover:rotate-360"
                style={{ transition: 'transform 0.3s ease' }}
              />
            </div>
          </div>
        </div>
      </section>

      {/* Connect With Me */}
      <section className="py-12 px-6 bg-white">
        <div className="max-w-4xl mx-auto text-center">
          <h2 className="text-3xl font-bold mb-6">📫 Connect With Me</h2>
          <p className="mb-6">Let's collaborate or chat about tech! Reach me through these animated links:</p>
          <div className="flex justify-center gap-6">
            <a href="mailto:your-email@example.com">
              <img
                src="https://img.icons8.com/?size=100&id=12580&format=png&color=000000 "
                alt="Email"
                className="w-12 transition-transform duration-300 hover:scale-125"
              />
            </a>
            <a href="https://linkedin.com/in/yourprofile ">
              <img
                src="https://img.icons8.com/?size=100&id=13930&format=png&color=000000 "
                alt="LinkedIn"
                className="w-12 transition-transform duration-300 hover:scale-125"
              />
            </a>
            <a href="https://your-portfolio-link.com ">
              <img
                src="https://img.icons8.com/?size=100&id=108784&format=png&color=000000 "
                alt="Portfolio"
                className="w-12 transition-transform duration-300 hover:scale-125"
              />
            </a>
          </div>
        </div>
      </section>

      {/* Fun Fact */}
      <section className="py-12 px-6 bg-gray-50 text-center">
        <h2 className="text-3xl font-bold mb-4">🎉 Fun Fact</h2>
        <p>Did you know? I once coded an entire project using only a mechanical keyboard with RGB lights to keep me motivated! 🌈</p>
      </section>

      {/* What's Next */}
      <footer className="py-8 px-6 bg-white text-center">
        <h2 className="text-2xl font-bold mb-4">🚀 What's Next?</h2>
        <p className="mb-4">Explore my repositories, star ⭐ your favorites, or drop me a message to collaborate on exciting projects. Thanks for visiting—let's create something amazing! 😄</p>
        <p className="text-sm text-gray-500">© 2025 Ahmad Raza | Made with ❤️ using React & Tailwind CSS</p>
      </footer>
    </div>
  );
}
