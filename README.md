<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Gilded Spoon | Fine Dining</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Configure Tailwind for a modern look -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'primary': '#4a2516', // Deep brown/maroon
                        'secondary': '#a0805c', // Aged brass/gold
                        'background': '#1a1a1a', // Dark charcoal
                        'text-light': '#f5f5f5', // Near white
                        'accent': '#d4af37', // Gold accent
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        serif: ['Georgia', 'serif'],
                    }
                }
            }
        }
    </script>
    <style>
        /* Custom styles for smooth transitions and background */
        body {
            background-color: #1a1a1a;
            color: #f5f5f5;
            font-family: 'Inter', sans-serif;
        }
        .page-content {
            transition: opacity 0.5s ease-in-out;
        }
        .hero-bg {
            background-image: url('https://placehold.co/1920x800/2a2a2a/f5f5f5?text=Elegant+Restaurant+Interior');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }
        .nav-link {
            cursor: pointer;
            transition: color 0.2s, background-color 0.2s, transform 0.2s;
        }
        .nav-link:hover {
            color: #d4af37;
            transform: translateY(-2px);
        }
        .active-link {
            color: #d4af37;
            border-bottom: 2px solid #d4af37;
            padding-bottom: 4px;
        }
    </style>
</head>
<body class="min-h-screen">

    <div id="app" class="flex flex-col min-h-screen">

        <!-- Header and Navigation -->
        <header class="bg-background shadow-lg sticky top-0 z-10 border-b border-secondary/20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex items-center justify-between h-20">
                    <!-- Logo/Brand -->
                    <div class="flex-shrink-0">
                        <span class="text-3xl font-serif font-bold text-accent tracking-widest">
                            The Gilded Spoon
                        </span>
                    </div>
                    <!-- Desktop Navigation -->
                    <nav class="hidden md:block">
                        <div class="ml-10 flex items-baseline space-x-8">
                            <span id="nav-home" class="nav-link text-text-light active-link font-medium text-lg" onclick="showPage('home')">Home</span>
                            <span id="nav-menu" class="nav-link text-text-light font-medium text-lg" onclick="showPage('menu')">Menu</span>
                            <span id="nav-about" class="nav-link text-text-light font-medium text-lg" onclick="showPage('about')">About Us</span>
                            <span id="nav-contact" class="nav-link text-text-light font-medium text-lg" onclick="showPage('contact')">Contact</span>
                            <a href="#" class="px-4 py-2 text-primary bg-accent rounded-full font-bold shadow-lg hover:bg-secondary transition duration-300 transform hover:scale-105">
                                Book A Table
                            </a>
                        </div>
                    </nav>
                    <!-- Mobile Menu Button (Hamburger) -->
                    <div class="md:hidden">
                        <button id="mobile-menu-btn" class="text-text-light hover:text-accent focus:outline-none" aria-label="Toggle menu">
                            <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                            </svg>
                        </button>
                    </div>
                </div>
            </div>

            <!-- Mobile Menu Dropdown -->
            <div id="mobile-menu" class="hidden md:hidden">
                <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3 flex flex-col">
                    <span class="nav-link text-text-light hover:bg-primary/50 block px-3 py-2 rounded-md text-base font-medium" onclick="showPage('home')">Home</span>
                    <span class="nav-link text-text-light hover:bg-primary/50 block px-3 py-2 rounded-md text-base font-medium" onclick="showPage('menu')">Menu</span>
                    <span class="nav-link text-text-light hover:bg-primary/50 block px-3 py-2 rounded-md text-base font-medium" onclick="showPage('about')">About Us</span>
                    <span class="nav-link text-text-light hover:bg-primary/50 block px-3 py-2 rounded-md text-base font-medium" onclick="showPage('contact')">Contact</span>
                    <a href="#" class="text-primary bg-accent block px-3 py-2 rounded-md text-base font-bold text-center mt-2">Book A Table</a>
                </div>
            </div>
        </header>

        <!-- Main Content Area -->
        <main class="flex-grow">
            <div class="max-w-7xl mx-auto py-8 px-4 sm:px-6 lg:px-8">

                <!-- 1. Home Page -->
                <section id="page-home" class="page-content">
                    <div class="hero-bg h-[70vh] flex items-center justify-center rounded-xl shadow-2xl mb-12">
                        <div class="text-center bg-background/70 p-8 rounded-xl backdrop-blur-sm border-2 border-accent/50">
                            <h1 class="text-6xl sm:text-7xl font-serif text-accent mb-4 leading-tight">
                                Taste the Tradition.
                            </h1>
                            <p class="text-xl text-text-light mb-8 max-w-lg mx-auto">
                                Where classic technique meets contemporary flavor. Experience fine dining at its best.
                            </p>
                            <button class="bg-accent text-primary font-bold py-3 px-8 rounded-full shadow-xl hover:bg-secondary/90 transition duration-300 text-lg" onclick="showPage('menu')">
                                View Our Full Menu
                            </button>
                        </div>
                    </div>

                    <div class="grid md:grid-cols-3 gap-8 text-center mt-16">
                        <div class="p-6 bg-primary/30 rounded-lg shadow-xl border border-secondary/30">
                            <h3 class="text-2xl font-serif text-accent mb-2">Artisan Dishes</h3>
                            <p class="text-secondary">Ingredients sourced daily from local farms.</p>
                        </div>
                        <div class="p-6 bg-primary/30 rounded-lg shadow-xl border border-secondary/30">
                            <h3 class="text-2xl font-serif text-accent mb-2">Master Sommelier</h3>
                            <p class="text-secondary">Perfect wine pairings for every course.</p>
                        </div>
                        <div class="p-6 bg-primary/30 rounded-lg shadow-xl border border-secondary/30">
                            <h3 class="text-2xl font-serif text-accent mb-2">Elegant Setting</h3>
                            <p class="text-secondary">The perfect ambiance for any occasion.</p>
                        </div>
                    </div>
                </section>

                <!-- 2. Menu Page (Hidden by default) -->
                <section id="page-menu" class="page-content hidden opacity-0">
                    <h2 class="text-5xl font-serif text-accent text-center mb-10 border-b pb-4 border-secondary/50">Our Culinary Offerings</h2>

                    <div class="space-y-12">
                        <!-- Appetizers -->
                        <div class="bg-background/80 p-6 rounded-xl shadow-2xl border border-primary/50">
                            <h3 class="text-4xl font-serif text-secondary mb-6 border-b pb-2 border-accent/20">Starters</h3>
                            <div class="grid md:grid-cols-2 gap-x-8 gap-y-6">
                                <div class="flex justify-between items-end border-b border-secondary/30 pb-2">
                                    <div>
                                        <p class="text-xl font-bold text-text-light">Seared Scallops</p>
                                        <p class="text-sm text-secondary">Lemon-butter reduction, microgreens.</p>
                                    </div>
                                    <span class="text-xl font-mono text-accent">$18</span>
                                </div>
                                <div class="flex justify-between items-end border-b border-secondary/30 pb-2">
                                    <div>
                                        <p class="text-xl font-bold text-text-light">Truffle Arancini</p>
                                        <p class="text-sm text-secondary">Aged parmesan, forest mushroom aioli.</p>
                                    </div>
                                    <span class="text-xl font-mono text-accent">$14</span>
                                </div>
                            </div>
                        </div>

                        <!-- Mains -->
                        <div class="bg-background/80 p-6 rounded-xl shadow-2xl border border-primary/50">
                            <h3 class="text-4xl font-serif text-secondary mb-6 border-b pb-2 border-accent/20">Entrées</h3>
                            <div class="grid md:grid-cols-2 gap-x-8 gap-y-6">
                                <div class="flex justify-between items-end border-b border-secondary/30 pb-2">
                                    <div>
                                        <p class="text-xl font-bold text-text-light">Filet Mignon</p>
                                        <p class="text-sm text-secondary">8oz center-cut, potato gratin, asparagus.</p>
                                    </div>
                                    <span class="text-xl font-mono text-accent">$48</span>
                                </div>
                                <div class="flex justify-between items-end border-b border-secondary/30 pb-2">
                                    <div>
                                        <p class="text-xl font-bold text-text-light">Pan-Roasted Halibut</p>
                                        <p class="text-sm text-secondary">Saffron risotto, blistered tomatoes, capers.</p>
                                    </div>
                                    <span class="text-xl font-mono text-accent">$42</span>
                                </div>
                                <div class="flex justify-between items-end border-b border-secondary/30 pb-2">
                                    <div>
                                        <p class="text-xl font-bold text-text-light">Vegetable Wellington</p>
                                        <p class="text-sm text-secondary">Seasonal root vegetables, puff pastry, herb sauce.</p>
                                    </div>
                                    <span class="text-xl font-mono text-accent">$32</span>
                                </div>
                            </div>
                        </div>

                        <!-- Desserts -->
                        <div class="bg-background/80 p-6 rounded-xl shadow-2xl border border-primary/50">
                            <h3 class="text-4xl font-serif text-secondary mb-6 border-b pb-2 border-accent/20">Desserts</h3>
                            <div class="grid md:grid-cols-2 gap-x-8 gap-y-6">
                                <div class="flex justify-between items-end border-b border-secondary/30 pb-2">
                                    <div>
                                        <p class="text-xl font-bold text-text-light">Chocolate Lava Cake</p>
                                        <p class="text-sm text-secondary">Raspberry coulis, vanilla bean ice cream.</p>
                                    </div>
                                    <span class="text-xl font-mono text-accent">$12</span>
                                </div>
                                <div class="flex justify-between items-end border-b border-secondary/30 pb-2">
                                    <div>
                                        <p class="text-xl font-bold text-text-light">Pistachio Tiramisu</p>
                                        <p class="text-sm text-secondary">Layered with espresso and mascarpone.</p>
                                    </div>
                                    <span class="text-xl font-mono text-accent">$11</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- 3. About Page (Hidden by default) -->
                <section id="page-about" class="page-content hidden opacity-0">
                    <h2 class="text-5xl font-serif text-accent text-center mb-10 border-b pb-4 border-secondary/50">Our Story: A Message from Chef Aiza Tahir</h2>

                    <div class="space-y-8 max-w-4xl mx-auto">
                        <div class="p-8 bg-primary/30 rounded-xl shadow-2xl border border-secondary/30">
                            <div class="md:flex md:space-x-8 items-start">
                                <div class="flex-shrink-0 mb-4 md:mb-0 text-center">
                                    <!-- Placeholder image for the chef -->
                                    <img src="https://placehold.co/150x150/4a2516/d4af37?text=Chef+A" alt="Chef Aiza Tahir" class="rounded-full object-cover w-32 h-32 mx-auto border-4 border-accent">
                                    <h3 class="text-2xl font-serif text-accent mt-3">Chef Aiza Tahir</h3>
                                </div>
                                <div class="flex-grow">
                                    <h3 class="text-3xl font-serif text-secondary mb-4">Passion and Dedication</h3>
                                    <p class="text-lg leading-relaxed">
                                        **I’m Aiza Tahir, a passionate chef dedicated to creating fresh, flavorful dishes inspired by my culinary journey.** I trained at top local kitchens and learned from experienced chefs who shaped my cooking style. My restaurant, The Gilded Spoon, here in **Gulberg, Lahore**, reflects my love for authentic taste and warm hospitality.
                                    </p>
                                    <p class="text-lg leading-relaxed mt-4">
                                        The Gilded Spoon is more than just a restaurant; it's the culmination of years spent perfecting classic techniques while embracing the vibrant ingredients found locally. We are committed to a dining experience that is both sophisticated and profoundly comforting.
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- 4. Contact Page (Hidden by default) -->
                <section id="page-contact" class="page-content hidden opacity-0">
                    <h2 class="text-5xl font-serif text-accent text-center mb-10 border-b pb-4 border-secondary/50">Find Us & Connect</h2>

                    <div class="grid lg:grid-cols-2 gap-8">
                        <!-- Location & Hours -->
                        <div class="p-8 bg-primary/30 rounded-xl shadow-2xl border border-secondary/30">
                            <h3 class="text-3xl font-serif text-secondary mb-4">Visit Us</h3>
                            <p class="text-lg mb-4">
                                **Address:** 15-B MM Alam Road, Gulberg, Lahore, Pakistan
                            </p>
                            <p class="text-lg mb-6">
                                **Reservations:** +92 42 111 555 123
                            </p>
                            <h3 class="text-3xl font-serif text-secondary mb-4">Hours</h3>
                            <ul class="space-y-2 text-lg">
                                <li>**Tuesday - Thursday:** 5:00 PM – 10:00 PM</li>
                                <li>**Friday - Saturday:** 5:00 PM – 11:00 PM</li>
                                <li>**Sunday:** Closed (Private Events Only)</li>
                                <li>**Monday:** Closed</li>
                            </ul>
                        </div>

                        <!-- Contact Form -->
                        <div class="p-8 bg-primary/30 rounded-xl shadow-2xl border border-secondary/30">
                            <h3 class="text-3xl font-serif text-secondary mb-4">Send Us a Message</h3>
                            <form action="#" method="POST" class="space-y-4">
                                <div>
                                    <label for="name" class="block text-sm font-medium text-text-light">Name</label>
                                    <input type="text" id="name" name="name" required class="mt-1 block w-full rounded-md border-gray-300 shadow-sm p-3 bg-background border border-secondary/50 text-text-light focus:ring-accent focus:border-accent">
                                </div>
                                <div>
                                    <label for="email" class="block text-sm font-medium text-text-light">Email</label>
                                    <input type="email" id="email" name="email" required class="mt-1 block w-full rounded-md border-gray-300 shadow-sm p-3 bg-background border border-secondary/50 text-text-light focus:ring-accent focus:border-accent">
                                </div>
                                <div>
                                    <label for="message" class="block text-sm font-medium text-text-light">Message</label>
                                    <textarea id="message" name="message" rows="4" required class="mt-1 block w-full rounded-md border-gray-300 shadow-sm p-3 bg-background border border-secondary/50 text-text-light focus:ring-accent focus:border-accent"></textarea>
                                </div>
                                <button type="submit" class="w-full bg-accent text-primary font-bold py-3 px-4 rounded-full shadow-lg hover:bg-secondary transition duration-300 transform hover:scale-[1.02]">
                                    Submit Inquiry
                                </button>
                            </form>
                        </div>
                    </div>
                </section>

            </div>
        </main>

        <!-- Footer -->
        <footer class="bg-background border-t border-secondary/20 mt-12 py-8">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <p class="text-secondary text-sm">
                    &copy; 2025 The Gilded Spoon. All rights reserved. | <a href="#" class="hover:text-accent transition">Privacy Policy</a>
                </p>
            </div>
        </footer>

    </div>

    <!-- JavaScript for Page Switching and Auth Boilerplate -->
    <script type="module">
        // Import Firebase modules
        import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
        import { getAuth, signInAnonymously, signInWithCustomToken, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";
        import { getFirestore, setLogLevel } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";

        // Firebase Boilerplate Setup (MANDATORY for Canvas Environment)
        const appId = typeof __app_id !== 'undefined' ? __app_id : 'default-app-id';
        const firebaseConfig = JSON.parse(typeof __firebase_config !== 'undefined' ? __firebase_config : '{}');
        const initialAuthToken = typeof __initial_auth_token !== 'undefined' ? __initial_auth_token : null;

        let app, db, auth;
        setLogLevel('debug'); // Enable debug logging for Firestore

        if (Object.keys(firebaseConfig).length > 0) {
            app = initializeApp(firebaseConfig);
            db = getFirestore(app);
            auth = getAuth(app);

            // Handle Authentication
            onAuthStateChanged(auth, (user) => {
                if (user) {
                    console.log("Firebase: User signed in with UID:", user.uid);
                } else {
                    console.log("Firebase: No user is signed in.");
                }
            });

            // Sign in using the custom token or anonymously
            (async () => {
                try {
                    if (initialAuthToken) {
                        await signInWithCustomToken(auth, initialAuthToken);
                        console.log("Firebase Auth: Signed in with custom token.");
                    } else {
                        await signInAnonymously(auth);
                        console.log("Firebase Auth: Signed in anonymously.");
                    }
                } catch (error) {
                    console.error("Firebase Auth Error:", error.message);
                }
            })();
        } else {
            console.warn("Firebase Config not found. Persistence is disabled.");
        }


        // Website Page Switching Logic

        const pages = ['home', 'menu', 'about', 'contact'];
        const pageElements = pages.map(id => document.getElementById(`page-${id}`));
        const navElements = pages.map(id => document.getElementById(`nav-${id}`));
        const mobileMenu = document.getElementById('mobile-menu');
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');

        // Toggle Mobile Menu
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        window.showPage = function(pageId) {
            // Hide all pages and remove active class from all links
            pageElements.forEach(el => {
                el.classList.add('hidden', 'opacity-0');
                el.classList.remove('opacity-100');
            });
            navElements.forEach(el => {
                el.classList.remove('active-link');
            });

            // Show the selected page and set active link
            const targetPage = document.getElementById(`page-${pageId}`);
            const targetNav = document.getElementById(`nav-${pageId}`);

            if (targetPage) {
                // Use a slight delay to ensure the opacity transition is visible
                setTimeout(() => {
                    targetPage.classList.remove('hidden');
                    // Force a reflow before applying opacity: 100
                    targetPage.offsetWidth; 
                    targetPage.classList.add('opacity-100');
                }, 10);
            }
            if (targetNav) {
                targetNav.classList.add('active-link');
            }

            // Close mobile menu after selection
            if (!mobileMenu.classList.contains('hidden')) {
                mobileMenu.classList.add('hidden');
            }
        }

        // Initialize the app to show the home page on load
        document.addEventListener('DOMContentLoaded', () => {
            // Check the current hash and navigate, otherwise default to 'home'
            const hash = window.location.hash.substring(1);
            if (pages.includes(hash)) {
                showPage(hash);
            } else {
                showPage('home');
            }
        });
    </script>
</body>
</html>
