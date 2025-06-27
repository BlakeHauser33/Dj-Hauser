# Dj-Hauser
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DJ [Your Name] - Official Website</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts - Inter for a clean look -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    <!-- Font Awesome for icons (social media, etc.) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" xintegrity="sha512-Fo3rlroJt2zB+wBwM/f1R1s+2h2A+o5+o6P/A+d6+o2+o3+o4+o5+o6/A+g2+g3+g4+g5+g6+g7/A+h2+h3+h4+h5+h6/A+i2+i3+i4+i5+i6/A+j2+j3+j4+j5+j6/A+k2+k3+k4+k5+k6/A+l2+l3+l4+l5+l6/A+m2+m3+m4+m5+m6/A+n2+n3+n4+n5+n6/A+o2+o3+o4+o5+o6/A+p2+p3+p4+p5+p6/A+q2+q3+q4+q5+q6/A+r2+r3+r4+r5+r6/A+s2+s3+s4+s5+s6/A+t2+t3+t4+t5+t6/A+u2+u3+u4+u5+u6/A+v2+v3+v4+v5+v6/A+w2+w3+w4+w5+w6/A+x2+x3+x4+x5+x6/A+y2+y3+y4+y5+y6/A+z2+z3+z4+z5+z6/A+02+03+04+05+06/A+12+13+14+15+16/A+22+23+24+25+26/A+32+33+34+35+36/A+42+43+44+45+46/A+52+53+54+55+56/A+62+63+64+65+66/A+72+73+74+75+76/A+82+83+84+85+86/A+92+93+94+95+96/A+A2+A3+A4+A5+A6/A+B2+B3+B4+B5+B6/A+C2+C3+C4+C5+C6/A+D2+D3+D4+D5+D6/A+E2+E3+E4+E5+E6/A+F2+F3+F4+F5+F6/A+G2+G3+G4+G5+G6/A+H2+H3+H4+H5+H6/A+I2+I3+I4+I5+I6/A+J2+J3+J4+J5+J6/A+K2+K3+K4+K5+K6/A+L2+L3+L4+L5+L6/A+M2+M3+M4+M5+M6/A+N2+N3+N4+N5+N6/A+O2+O3+O4+O5+O6/A+P2+P3+P4+P5+P6/A+Q2+Q3+Q4+Q5+Q6/A+R2+R3+R4+R5+R6/A+S2+S3+S4+S5+S6/A+T2+T3+T4+T5+T6/A+U2+U3+U4+U5+U6/A+V2+V3+V4+V5+V6/A+W2+W3+W4+W5+W6/A+X2+X3+X4+X5+X6/A+Y2+Y3+Y4+Y5+Y6/A+Z2+Z3+Z4+Z5+Z6" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <style>
        /* Optional: Smooth scroll for navigation */
        html {
            scroll-behavior: smooth;
        }
        body {
            font-family: 'Inter', sans-serif;
        }
        /* Custom gradient background for buttons or sections */
        .gradient-button {
            background-image: linear-gradient(to right, #4ade80, #2dd4bf, #06b6d4); /* green-400 to cyan-400 to sky-500 */
            transition: all 0.3s ease-in-out;
        }
        .gradient-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05); /* shadow-lg */
        }
        /* Hero section specific style for background image */
        #hero {
            background-attachment: fixed; /* Parallax effect */
        }
        /* Styling for the mobile navigation toggle */
        #mobile-menu-button span {
            display: block;
            width: 25px;
            height: 3px;
            background-color: white;
            margin-bottom: 5px;
            transition: all 0.3s ease-in-out;
        }
        #mobile-menu-button.open span:nth-child(1) {
            transform: rotate(45deg) translate(5px, 5px);
        }
        #mobile-menu-button.open span:nth-child(2) {
            opacity: 0;
        }
        #mobile-menu-button.open span:nth-child(3) {
            transform: rotate(-45deg) translate(5px, -5px);
        }
        @media (max-width: 767px) {
            #main-nav {
                display: none;
            }
            #main-nav.active {
                display: flex;
                flex-direction: column;
                position: absolute;
                top: 80px; /* Adjust based on header height */
                left: 0;
                width: 100%;
                background-color: rgba(17, 24, 39, 0.95); /* bg-gray-900 with transparency */
                padding: 1rem 0;
                box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            }
            #main-nav.active li {
                margin: 0.5rem 0;
                text-align: center;
            }
        }
    </style>
</head>
<body class="bg-gray-900 text-white leading-relaxed">

    <!-- Header Section -->
    <header class="bg-gray-900 p-4 md:p-6 shadow-xl fixed w-full z-20 top-0">
        <div class="container mx-auto flex justify-between items-center flex-wrap">
            <h1 class="text-3xl md:text-4xl font-extrabold text-sky-400 tracking-wide">DJ [YOUR NAME]</h1>
            <!-- Mobile Menu Button -->
            <button id="mobile-menu-button" class="md:hidden p-2 rounded-md focus:outline-none focus:ring-2 focus:ring-sky-400">
                <span></span>
                <span></span>
                <span></span>
            </button>
            <nav id="main-nav" class="hidden md:flex flex-grow justify-end">
                <ul class="flex flex-col md:flex-row md:space-x-8 text-lg font-medium">
                    <li><a href="#about" class="block py-2 px-4 rounded-lg hover:bg-gray-700 transition-colors duration-300">About</a></li>
                    <li><a href="#skills" class="block py-2 px-4 rounded-lg hover:bg-gray-700 transition-colors duration-300">My Skills</a></li>
                    <li><a href="#mixes" class="block py-2 px-4 rounded-lg hover:bg-gray-700 transition-colors duration-300">Mixes</a></li>
                    <li><a href="#gallery" class="block py-2 px-4 rounded-lg hover:bg-gray-700 transition-colors duration-300">Gallery</a></li>
                    <li><a href="#contact" class="block py-2 px-4 rounded-lg hover:bg-gray-700 transition-colors duration-300">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="hero" class="relative h-screen flex items-center justify-center text-center bg-cover bg-center" style="background-image: url('https://placehold.co/1920x1080/1a1a1a/ffffff?text=Your+Epic+DJ+Background');">
        <!-- Overlay for better text readability -->
        <div class="absolute inset-0 bg-black opacity-70"></div>
        <div class="relative z-10 p-6 md:p-10 max-w-4xl mx-auto">
            <h2 class="text-4xl md:text-6xl lg:text-7xl font-extrabold leading-tight text-white drop-shadow-lg animate-fade-in-up">
                Igniting Dance Floors, Crafting Sonic Journeys.
            </h2>
            <p class="mt-4 md:mt-6 text-lg md:text-xl text-gray-300 animate-fade-in-up delay-200">
                Experience the beats that transcend boundaries and elevate every moment.
            </p>
            <a href="#mixes" class="mt-8 inline-block py-3 px-8 rounded-full text-lg font-bold text-white gradient-button shadow-lg">
                Discover My Sound
            </a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-16 md:py-24 bg-gray-800">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-4xl md:text-5xl font-bold text-sky-400 mb-10">About Me</h2>
            <div class="max-w-4xl mx-auto text-lg text-gray-300">
                <p class="mb-6">
                    Hello! I'm DJ [Your Name], a passionate electronic music artist and performer dedicated to
                    creating unforgettable auditory experiences. My journey began [e.g., years ago in your hometown],
                    fueled by a deep love for rhythm, melody, and the unifying power of sound.
                </p>
                <p class="mb-6">
                    From intimate gatherings to large-scale events, I specialize in curating sets that read and
                    respond to the energy of the crowd. My influences span a wide spectrum of genres, allowing me
                    to seamlessly blend tracks and build dynamic narratives through music.
                </p>
                <p>
                    When I'm not behind the decks, I'm constantly exploring new sounds, refining my techniques, and
                    producing original tracks. I believe every set is an opportunity to connect, inspire, and create
                    a shared memory through the universal language of music.
                </p>
            </div>
        </div>
    </section>

    <!-- My Skills/What I Can Do Section -->
    <section id="skills" class="py-16 md:py-24 bg-gray-900">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-4xl md:text-5xl font-bold text-sky-400 mb-10">What I Bring to the Table</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-5xl mx-auto">
                <div class="bg-gray-800 p-8 rounded-xl shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
                    <i class="fas fa-headphones-alt text-5xl text-teal-400 mb-4"></i>
                    <h3 class="text-2xl font-semibold text-white mb-3">Expert Mixology</h3>
                    <p class="text-gray-300">Seamless transitions, creative track selections, and precise beatmatching to keep the energy flowing.</p>
                </div>
                <div class="bg-gray-800 p-8 rounded-xl shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
                    <i class="fas fa-users text-5xl text-teal-400 mb-4"></i>
                    <h3 class="text-2xl font-semibold text-white mb-3">Crowd Reading</h3>
                    <p class="text-gray-300">Ability to sense the room's vibe and adapt the set in real-time, ensuring maximum engagement.</p>
                </div>
                <div class="bg-gray-800 p-8 rounded-xl shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
                    <i class="fas fa-music text-5xl text-teal-400 mb-4"></i>
                    <h3 class="text-2xl font-semibold text-white mb-3">Genre Versatility</h3>
                    <p class="text-gray-300">Proficiency across a wide range of genres including House, Techno, Hip-Hop, R&B, and Open Format.</p>
                </div>
                <div class="bg-gray-800 p-8 rounded-xl shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
                    <i class="fas fa-microphone-alt text-5xl text-teal-400 mb-4"></i>
                    <h3 class="text-2xl font-semibold text-white mb-3">MC & Hosting</h3>
                    <p class="text-gray-300">Capable of engaging the audience on the microphone, hosting events, and making announcements.</p>
                </div>
                <div class="bg-gray-800 p-8 rounded-xl shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
                    <i class="fas fa-bolt text-5xl text-teal-400 mb-4"></i>
                    <h3 class="text-2xl font-semibold text-white mb-3">Energy & Presence</h3>
                    <p class="text-gray-300">Dynamic stage presence and an infectious energy that radiates throughout the venue.</p>
                </div>
                <div class="bg-gray-800 p-8 rounded-xl shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
                    <i class="fas fa-laptop-code text-5xl text-teal-400 mb-4"></i>
                    <h3 class="text-2xl font-semibold text-white mb-3">Technical Proficiency</h3>
                    <p class="text-gray-300">Adept with various DJ equipment, software, and sound systems for seamless setup and performance.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Mixes Section -->
    <section id="mixes" class="py-16 md:py-24 bg-gray-800">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-4xl md:text-5xl font-bold text-sky-400 mb-12">My Latest Mixes & Sets</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
                <!-- Mix 1 Placeholder -->
                <div class="bg-gray-900 p-6 rounded-lg shadow-xl border border-gray-700 hover:border-sky-400 transition-all duration-300">
                    <h3 class="text-2xl font-semibold mb-4 text-white">[Mix Title 1] - Live at [Venue Name]</h3>
                    <!-- REPLACE THIS IFRAME with your actual SoundCloud, Mixcloud, or YouTube embed code -->
                    <iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/YOUR_SOUNDCLOUD_TRACK_ID_1&color=%2306b6d4&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>
                    <p class="text-gray-400 mt-4 text-base">An electrifying journey through deep house and melodic techno, recorded live on [Date].</p>
                </div>
                <!-- Mix 2 Placeholder -->
                <div class="bg-gray-900 p-6 rounded-lg shadow-xl border border-gray-700 hover:border-sky-400 transition-all duration-300">
                    <h3 class="text-2xl font-semibold mb-4 text-white">[Mix Title 2] - Weekend Vibes</h3>
                    <!-- REPLACE THIS IFRAME with your actual SoundCloud, Mixcloud, or YouTube embed code -->
                    <iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/YOUR_SOUNDCLOUD_TRACK_ID_2&color=%2306b6d4&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>
                    <p class="text-gray-400 mt-4 text-base">A compilation of high-energy hip-hop and R&B tracks perfect for your next party.</p>
                </div>
                <!-- Mix 3 Placeholder -->
                <div class="bg-gray-900 p-6 rounded-lg shadow-xl border border-gray-700 hover:border-sky-400 transition-all duration-300">
                    <h3 class="text-2xl font-semibold mb-4 text-white">[Mix Title 3] - Chill Out Session</h3>
                    <!-- REPLACE THIS IFRAME with your actual SoundCloud, Mixcloud, or YouTube embed code -->
                    <iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/YOUR_SOUNDCLOUD_TRACK_ID_3&color=%2306b6d4&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>
                    <p class="text-gray-400 mt-4 text-base">Unwind with this smooth selection of downtempo and soulful electronic beats.</p>
                </div>
                <!-- Add more mix placeholders by copying and pasting the div above -->
            </div>
            <p class="text-gray-400 mt-12 text-lg">
                For my full catalog of mixes and live sets, visit my
                <a href="YOUR_SOUNDCLOUD_OR_MIXCLOUD_PROFILE_LINK" target="_blank" class="text-sky-400 hover:text-sky-300 underline font-semibold">SoundCloud/Mixcloud profile</a>!
            </p>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="py-16 md:py-24 bg-gray-900">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-4xl md:text-5xl font-bold text-sky-400 mb-12">Capture the Moment: Photo Gallery</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8">
                <!-- Photo Placeholder 1 -->
                <div class="rounded-xl overflow-hidden shadow-xl border border-gray-700 hover:border-teal-400 transform hover:scale-105 transition-all duration-300">
                    <img src="https://placehold.co/600x400/222222/FFFFFF?text=Live+Performance+1" alt="DJ Live Performance" class="w-full h-auto object-cover">
                </div>
                <!-- Photo Placeholder 2 -->
                <div class="rounded-xl overflow-hidden shadow-xl border border-gray-700 hover:border-teal-400 transform hover:scale-105 transition-all duration-300">
                    <img src="https://placehold.co/600x400/333333/FFFFFF?text=Studio+Session" alt="DJ in Studio" class="w-full h-auto object-cover">
                </div>
                <!-- Photo Placeholder 3 -->
                <div class="rounded-xl overflow-hidden shadow-xl border border-gray-700 hover:border-teal-400 transform hover:scale-105 transition-all duration-300">
                    <img src="https://placehold.co/600x400/444444/FFFFFF?text=Crowd+View" alt="Crowd at DJ event" class="w-full h-auto object-cover">
                </div>
                <!-- Photo Placeholder 4 -->
                <div class="rounded-xl overflow-hidden shadow-xl border border-gray-700 hover:border-teal-400 transform hover:scale-105 transition-all duration-300">
                    <img src="https://placehold.co/600x400/555555/FFFFFF?text=DJ+Gear" alt="DJ Equipment" class="w-full h-auto object-cover">
                </div>
                <!-- Add more photo placeholders by copying and pasting the div above -->
            </div>
            <p class="text-gray-400 mt-12 text-lg">
                Follow me on <a href="YOUR_INSTAGRAM_LINK" target="_blank" class="text-sky-400 hover:text-sky-300 underline font-semibold">Instagram</a>
                for more behind-the-scenes content and live event photos!
            </p>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 md:py-24 bg-gray-800">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-4xl md:text-5xl font-bold text-sky-400 mb-10">Let's Connect!</h2>
            <p class="text-xl text-gray-300 mb-8 max-w-2xl mx-auto">
                Whether you're looking to book me for an event, collaborate on a project, or just say hello,
                I'd love to hear from you!
            </p>
            <div class="max-w-xl mx-auto bg-gray-900 p-8 rounded-xl shadow-xl border border-gray-700">
                <p class="text-lg text-gray-300 mb-4">Send me an email:</p>
                <a href="mailto:your.email@example.com" class="text-sky-400 hover:text-sky-300 text-2xl md:text-3xl font-bold mb-6 block break-all">
                    your.email@example.com
                </a>

                <p class="text-lg text-gray-300 mb-4 mt-8">Find me on social media:</p>
                <div class="flex justify-center space-x-6 md:space-x-8 text-4xl">
                    <a href="YOUR_INSTAGRAM_LINK" target="_blank" class="text-gray-400 hover:text-pink-500 transition-colors duration-300">
                        <i class="fab fa-instagram"></i>
                    </a>
                    <a href="YOUR_FACEBOOK_LINK" target="_blank" class="text-gray-400 hover:text-blue-600 transition-colors duration-300">
                        <i class="fab fa-facebook"></i>
                    </a>
                    <a href="YOUR_TWITTER_LINK" target="_blank" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">
                        <i class="fab fa-twitter"></i>
                    </a>
                    <a href="YOUR_SOUNDCLOUD_LINK" target="_blank" class="text-gray-400 hover:text-orange-500 transition-colors duration-300">
                        <i class="fab fa-soundcloud"></i>
                    </a>
                    <a href="YOUR_MIXCLOUD_LINK" target="_blank" class="text-gray-400 hover:text-purple-600 transition-colors duration-300">
                        <i class="fab fa-mixcloud"></i>
                    </a>
                    <!-- Add more social links as needed (e.g., YouTube, TikTok) -->
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 py-8 text-center text-gray-500 text-sm">
        <div class="container mx-auto px-6">
            &copy; 2025 DJ [YOUR NAME]. All rights reserved. | Crafted with passion.
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                // Close mobile menu if open
                if (window.innerWidth < 768) {
                    const nav = document.getElementById('main-nav');
                    const button = document.getElementById('mobile-menu-button');
                    nav.classList.remove('active');
                    button.classList.remove('open');
                }
            });
        });

        // Mobile menu toggle functionality
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mainNav = document.getElementById('main-nav');

        mobileMenuButton.addEventListener('click', () => {
            mainNav.classList.toggle('active');
            mobileMenuButton.classList.toggle('open');
        });

        // Close mobile menu when clicking outside (optional, but good for UX)
        document.addEventListener('click', (event) => {
            const isClickInsideNav = mainNav.contains(event.target);
            const isClickOnButton = mobileMenuButton.contains(event.target);

            if (!isClickInsideNav && !isClickOnButton && mainNav.classList.contains('active')) {
                mainNav.classList.remove('active');
                mobileMenuButton.classList.remove('open');
            }
        });
    </script>

</body>
</html>
