EduLearn - Educational Platform function showInfo

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EduLearn - Educational Platform</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        function showInfo(title, content) {
            document.getElementById('modal-title').innerText = title;
            document.getElementById('modal-content').innerText = content;
            document.getElementById('info-modal').classList.remove('hidden');
        }
        function closeModal() {
            document.getElementById('info-modal').classList.add('hidden');
        }
    </script>
</head>
<body class="bg-gray-50 text-gray-900">
    <!-- Navbar -->
    <nav class="bg-white shadow p-4 flex justify-between items-center sticky top-0 z-50">
        <h1 class="text-2xl font-bold text-blue-600">EduLearn</h1>
        <div class="space-x-4">
            <a href="#home" class="hover:text-blue-600">Home</a>
            <a href="#articles" class="hover:text-blue-600">Articles</a>
            <a href="#courses" class="hover:text-blue-600">Courses</a>
            <a href="#about" class="hover:text-blue-600">About</a>
            <a href="#dashboard" class="hover:text-blue-600">Dashboard</a>
        </div>
    </nav>

    <!-- Homepage -->
    <section id="home" class="p-8 text-center bg-gradient-to-r from-blue-100 to-blue-50">
        <h2 class="text-3xl font-bold mb-4">Welcome to EduLearn</h2>
        <p class="mb-6">Explore featured articles, top courses, and guides for your learning journey.</p>
        <input type="text" placeholder="Search by topic or grade..." class="border rounded p-2 w-2/3 max-w-lg">
        <div class="mt-6">
            <button class="bg-blue-600 text-white px-6 py-2 rounded shadow hover:bg-blue-700">Start Learning</button>
        </div>
        <div class="grid md:grid-cols-2 gap-6 mt-10">
            <div class="bg-white p-4 rounded shadow">
                <img src="https://via.placeholder.com/400x200" class="rounded mb-3" alt="Data Science Basics">
                <h3 class="text-xl font-semibold">Featured Article: Data Science Basics</h3>
                <p class="text-sm mt-2">An introduction to data science tools, techniques, and applications.</p>
                <button onclick="showInfo('Data Science Basics', 'This article introduces you to data science concepts, tools like Python, and career paths.')" class="text-blue-600 mt-4">Read More</button>
            </div>
            <div class="bg-white p-4 rounded shadow">
                <img src="https://via.placeholder.com/400x200" class="rounded mb-3" alt="Linux for Beginners">
                <h3 class="text-xl font-semibold">Featured Course: Linux for Beginners</h3>
                <p class="text-sm mt-2">Learn Linux fundamentals and get comfortable with Ubuntu setup.</p>
                <button onclick="showInfo('Linux for Beginners', 'This course covers Linux commands, terminal basics, and Ubuntu installation guides.')" class="text-blue-600 mt-4">View Course</button>
            </div>
        </div>
    </section>

    <!-- Articles Page -->
    <section id="articles" class="p-8 bg-gray-100">
        <h2 class="text-2xl font-bold mb-4">Articles by Subject</h2>
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
            <div class="bg-white p-4 rounded shadow">
                <h3 class="font-semibold">Language Learning Tips</h3>
                <p class="text-sm mt-2">Enhance your language proficiency with proven techniques.</p>
                <button onclick="showInfo('Language Learning Tips', 'Detailed article on improving language skills, recommended apps, and exercises.')" class="text-blue-600 mt-3 block">Related Courses & Setup Guides</button>
            </div>
            <div class="bg-white p-4 rounded shadow">
                <h3 class="font-semibold">Data Science Explained</h3>
                <p class="text-sm mt-2">Understand AI, ML, and data handling to build your career.</p>
                <button onclick="showInfo('Data Science Explained', 'Comprehensive guide on data analysis, AI models, and starting a data science career.')" class="text-blue-600 mt-3 block">Related Courses & Setup Guides</button>
            </div>
            <div class="bg-white p-4 rounded shadow">
                <h3 class="font-semibold">Operating Linux & Ubuntu</h3>
                <p class="text-sm mt-2">Master Linux commands and set up Ubuntu step-by-step.</p>
                <button onclick="showInfo('Operating Linux & Ubuntu', 'Step-by-step OS setup guide including installation, command-line basics, and configuration.')" class="text-blue-600 mt-3 block">Setup Operating System Guide</button>
            </div>
        </div>
    </section>

    <!-- Courses Page -->
    <section id="courses" class="p-8">
        <h2 class="text-2xl font-bold mb-4">Course Catalog</h2>
        <div class="flex gap-4 mb-6 flex-wrap">
            <select class="border p-2 rounded">
                <option>All Subjects</option>
                <option>Language</option>
                <option>Data Science</option>
                <option>Linux/Ubuntu</option>
            </select>
            <select class="border p-2 rounded">
                <option>All Levels</option>
                <option>Beginner</option>
                <option>Intermediate</option>
                <option>Advanced</option>
            </select>
            <select class="border p-2 rounded">
                <option>Format: All</option>
                <option>Video</option>
                <option>PDF</option>
                <option>Quiz</option>
                <option>Setup Code/Command</option>
            </select>
        </div>
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
            <div class="bg-white p-4 rounded shadow">
                <h3 class="font-semibold">Intro to Data Science</h3>
                <p class="text-sm mt-2">A beginner-friendly series with videos, PDFs, and code snippets.</p>
                <button onclick="showInfo('Intro to Data Science', 'Downloadable materials, video tutorials, and practice datasets included.')" class="text-blue-600 mt-4">View Details</button>
            </div>
            <div class="bg-white p-4 rounded shadow">
                <h3 class="font-semibold">Ubuntu Mastery & Setup</h3>
                <p class="text-sm mt-2">Step-by-step OS setup guide with downloadable commands and videos.</p>
                <button onclick="showInfo('Ubuntu Mastery & Setup', 'Includes terminal commands, configuration files, and video walkthroughs.')" class="text-blue-600 mt-4">View Details</button>
            </div>
        </div>
    </section>

    <!-- About & Contact Page -->
    <section id="about" class="p-8 bg-gray-100">
        <h2 class="text-2xl font-bold mb-4">About EduLearn</h2>
        <p class="mb-4">EduLearn provides accessible and high-quality content for learners and educators worldwide, covering articles, courses, and OS setup guides.</p>
        <h3 class="text-xl font-semibold mb-2">Contact Us</h3>
        <form class="grid gap-4 max-w-md">
            <input type="text" placeholder="Your Name" class="border p-2 rounded">
            <input type="email" placeholder="Your Email" class="border p-2 rounded">
            <textarea placeholder="Your Message" class="border p-2 rounded"></textarea>
            <button class="bg-blue-600 text-white px-4 py-2 rounded">Send Message</button>
        </form>
    </section>

    <!-- User Dashboard (Skeleton) -->
    <section id="dashboard" class="p-8">
        <h2 class="text-2xl font-bold mb-4">User Dashboard</h2>
        <p class="text-sm">Login to save your favorite articles and track course progress. Dashboard features will include saved content, progress tracking, and recommended courses. (Coming soon)</p>
    </section>

    <!-- Info Modal -->
    <div id="info-modal" class="hidden fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4">
        <div class="bg-white p-6 rounded shadow max-w-lg w-full">
            <h3 id="modal-title" class="text-xl font-bold mb-4"></h3>
            <p id="modal-content" class="mb-4"></p>
            <button onclick="closeModal()" class="bg-blue-600 text-white px-4 py-2 rounded">Close</button>
        </div>
    </div>
</body>
</html>
