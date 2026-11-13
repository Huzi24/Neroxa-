# Neroxa-

<!DOCTYPE html>
<html lang="en" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nexora — AI & Productivity Hub</title>
    <meta name="description" content="Professional AI-powered services, productivity tools, developer utilities, and content creation hub.">
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        navy: { 900: '#0B0F19', 800: '#111827', 700: '#1F2937', 600: '#374151' },
                        electric: { 500: '#3B82F6', 600: '#2563EB' },
                        violet: { 500: '#8B5CF6', 600: '#7C3AED' },
                        cyan: { 400: '#22D3EE', 500: '#06B6D4' }
                    }
                }
            }
        }
    </script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
</head>
<body class="bg-navy-900 text-gray-100 font-sans antialiased selection:bg-electric-500 selection:text-white min-h-screen flex flex-col">
    <!-- Top Announcement Banner -->
    <div class="bg-gradient-to-r from-electric-600 via-violet-600 to-cyan-500 text-white text-xs font-semibold py-2 px-4 text-center">
        🚀 Nexora v2.5 Enterprise Edition Live — Experience Advanced AI Workflows, Cloud Sync & Developer Utilities! 
        <a href="#tools" onclick="switchTab('tools')" class="underline ml-2 hover:text-gray-200">Explore Tools &rarr;</a>
    </div>

    <!-- Navigation Bar -->
    <header class="sticky top-0 z-50 backdrop-blur-md bg-navy-900/80 border-b border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <div class="flex items-center space-x-3 cursor-pointer" onclick="switchTab('home')">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-electric-500 to-cyan-400 flex items-center justify-center shadow-lg shadow-electric-500/30">
                    <i class="fa-solid fa-cube text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold bg-gradient-to-r from-white via-gray-200 to-cyan-400 bg-clip-text text-transparent">Nexora</span>
            </div>

            <nav class="hidden md:flex items-center space-x-8 text-sm font-medium">
                <button onclick="switchTab('home')" class="nav-link text-electric-400 transition hover:text-electric-400">Home</button>
                <button onclick="switchTab('tools')" class="nav-link text-gray-300 transition hover:text-electric-400">Tools Hub</button>
                <button onclick="switchTab('dashboard')" class="nav-link text-gray-300 transition hover:text-electric-400">Dashboard</button>
                <button onclick="switchTab('blog')" class="nav-link text-gray-300 transition hover:text-electric-400">Blog & Guides</button>
                <button onclick="switchTab('pricing')" class="nav-link text-gray-300 transition hover:text-electric-400">Pricing</button>
                <button onclick="switchTab('about')" class="nav-link text-gray-300 transition hover:text-electric-400">About</button>
                <button onclick="switchTab('contact')" class="nav-link text-gray-300 transition hover:text-electric-400">Contact</button>
            </nav>

            <div class="flex items-center space-x-4">
                <button onclick="toggleTheme()" class="w-9 h-9 rounded-lg bg-navy-800 border border-gray-700 flex items-center justify-center text-gray-300 hover:text-white transition">
                    <i id="theme-icon" class="fa-solid fa-moon"></i>
                </button>
                <button onclick="openAuthModal('login')" class="hidden sm:inline-flex px-4 py-2 rounded-lg bg-navy-800 border border-gray-700 text-sm font-medium hover:bg-navy-700 transition">Sign In</button>
                <button onclick="openAuthModal('register')" class="px-4 py-2 rounded-lg bg-gradient-to-r from-electric-500 to-violet-600 text-sm font-medium text-white shadow-lg shadow-electric-500/20 hover:opacity-90 transition">Get Started</button>
                <button onclick="toggleMobileMenu()" class="md:hidden text-gray-300 focus:outline-none"><i class="fa-solid fa-bars text-xl"></i></button>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-navy-800 border-b border-gray-700 px-4 py-4 space-y-3">
            <button onclick="switchTab('home'); toggleMobileMenu()" class="block w-full text-left py-2 text-gray-200">Home</button>
            <button onclick="switchTab('tools'); toggleMobileMenu()" class="block w-full text-left py-2 text-gray-200">Tools Hub</button>
            <button onclick="switchTab('dashboard'); toggleMobileMenu()" class="block w-full text-left py-2 text-gray-200">Dashboard</button>
            <button onclick="switchTab('blog'); toggleMobileMenu()" class="block w-full text-left py-2 text-gray-200">Blog & Guides</button>
            <button onclick="switchTab('pricing'); toggleMobileMenu()" class="block w-full text-left py-2 text-gray-200">Pricing</button>
            <button onclick="switchTab('about'); toggleMobileMenu()" class="block w-full text-left py-2 text-gray-200">About</button>
            <button onclick="switchTab('contact'); toggleMobileMenu()" class="block w-full text-left py-2 text-gray-200">Contact</button>
        </div>
    </header>

    <!-- Main Content Area -->
    <main class="flex-grow">
        <!-- HOME VIEW -->
        <div id="view-home" class="view-section">
            <section class="relative overflow-hidden py-24 sm:py-32">
                <div class="absolute inset-0 bg-[radial-gradient(ellipse_at_top,_var(--tw-gradient-stops))] from-blue-950/40 via-navy-900 to-navy-900 pointer-events-none"></div>
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10 text-center">
                    <div class="inline-flex items-center space-x-2 px-3 py-1 rounded-full bg-electric-500/10 border border-electric-500/30 text-electric-400 text-xs font-semibold mb-6">
                        <i class="fa-solid fa-wand-magic-sparkles"></i>
                        <span>Next-Gen AI & Developer Ecosystem</span>
                    </div>
                    <h1 class="text-4xl sm:text-6xl lg:text-7xl font-extrabold tracking-tight max-w-4xl mx-auto leading-tight">
                        Empowering Productivity with <span class="bg-gradient-to-r from-electric-400 via-violet-400 to-cyan-400 bg-clip-text text-transparent">Intelligence</span>
                    </h1>
                    <p class="mt-6 text-lg sm:text-xl text-gray-400 max-w-2xl mx-auto">
                        Access professional AI workflows, instant developer utilities, content planning suites, and robust productivity calculators in one unified SaaS workspace.
                    </p>
                    <div class="mt-10 flex flex-col sm:flex-row justify-center items-center space-y-4 sm:space-y-0 sm:space-x-4">
                        <button onclick="switchTab('tools')" class="w-full sm:w-auto px-8 py-4 rounded-xl bg-gradient-to-r from-electric-500 to-violet-600 text-white font-semibold shadow-xl shadow-electric-500/25 hover:opacity-95 transition flex items-center justify-center space-x-2">
                            <span>Explore Tools Hub</span>
                            <i class="fa-solid fa-arrow-right"></i>
                        </button>
                        <button onclick="openAuthModal('register')" class="w-full sm:w-auto px-8 py-4 rounded-xl bg-navy-800 border border-gray-700 text-gray-200 font-semibold hover:bg-navy-700 transition">
                            Create Free Account
                        </button>
                    </div>

                    <!-- Stats Bar -->
                    <div class="mt-20 grid grid-cols-2 md:grid-cols-4 gap-6 max-w-4xl mx-auto border-t border-b border-gray-800 py-8">
                        <div>
                            <div class="text-3xl font-extrabold text-white">12+</div>
                            <div class="text-xs text-gray-400 mt-1 uppercase tracking-wider">Active Utilities</div>
                        </div>
                        <div>
                            <div class="text-3xl font-extrabold text-white">99.9%</div>
                            <div class="text-xs text-gray-400 mt-1 uppercase tracking-wider">Uptime Reliability</div>
                        </div>
                        <div>
                            <div class="text-3xl font-extrabold text-white">Zero</div>
                            <div class="text-xs text-gray-400 mt-1 uppercase tracking-wider">Client-Side Latency</div>
                        </div>
                        <div>
                            <div class="text-3xl font-extrabold text-white">Secure</div>
                            <div class="text-xs text-gray-400 mt-1 uppercase tracking-wider">BYOK AI Architecture</div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Featured Tools Preview Grid -->
            <section class="py-20 bg-navy-800/50 border-t border-gray-800">
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                    <div class="flex justify-between items-end mb-12">
                        <div>
                            <h2 class="text-2xl sm:text-3xl font-bold">Featured Professional Tools</h2>
                            <p class="text-gray-400 text-sm mt-1">Instant browser-side utilities built for speed and accuracy.</p>
                        </div>
                        <button onclick="switchTab('tools')" class="text-electric-400 hover:text-electric-300 text-sm font-semibold flex items-center space-x-1">
                            <span>View All Tools</span>
                            <i class="fa-solid fa-chevron-right text-xs"></i>
                        </button>
                    </div>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                        <div class="bg-navy-800 border border-gray-700/80 rounded-2xl p-6 hover:border-electric-500/50 transition cursor-pointer" onclick="openTool('word-counter')">
                            <div class="w-12 h-12 rounded-xl bg-electric-500/10 text-electric-400 flex items-center justify-center text-xl mb-4"><i class="fa-solid fa-file-lines"></i></div>
                            <h3 class="text-lg font-semibold text-white">Word & Character Counter</h3>
                            <p class="text-gray-400 text-sm mt-2">Instant count metrics, reading time estimator, and density checks.</p>
                        </div>
                        <div class="bg-navy-800 border border-gray-700/80 rounded-2xl p-6 hover:border-electric-500/50 transition cursor-pointer" onclick="openTool('password-gen')">
                            <div class="w-12 h-12 rounded-xl bg-violet-500/10 text-violet-400 flex items-center justify-center text-xl mb-4"><i class="fa-solid fa-shield-halved"></i></div>
                            <h3 class="text-lg font-semibold text-white">Password Strength & Generator</h3>
                            <p class="text-gray-400 text-sm mt-2">Create cryptographic secure passwords and test entropy scores.</p>
                        </div>
                        <div class="bg-navy-800 border border-gray-700/80 rounded-2xl p-6 hover:border-electric-500/50 transition cursor-pointer" onclick="openTool('json-formatter')">
                            <div class="w-12 h-12 rounded-xl bg-cyan-500/10 text-cyan-400 flex items-center justify-center text-xl mb-4"><i class="fa-solid fa-code"></i></div>
                            <h3 class="text-lg font-semibold text-white">JSON & Code Formatter</h3>
                            <p class="text-gray-400 text-sm mt-2">Validate, beautify, and minify JSON payloads instantly.</p>
                        </div>
                    </div>
                </div>
            </section>
        </div>

        <!-- TOOLS HUB VIEW -->
        <div id="view-tools" class="view-section hidden py-16">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-3xl mx-auto mb-12">
                    <h1 class="text-3xl sm:text-4xl font-bold">Comprehensive Tools Hub</h1>
                    <p class="text-gray-400 mt-2">Select from our suite of professional client-side utilities.</p>
                    <div class="mt-6 relative max-w-xl mx-auto">
                        <i class="fa-solid fa-search absolute left-4 top-3.5 text-gray-500"></i>
                        <input type="text" id="tool-search" oninput="filterTools()" placeholder="Search utilities (e.g. JSON, QR, Password, Counter)..." class="w-full bg-navy-800 border border-gray-700 rounded-xl pl-11 pr-4 py-3 text-sm text-white focus:outline-none focus:border-electric-500">
                    </div>
                </div>

                <!-- Category Pills -->
                <div class="flex flex-wrap justify-center gap-2 mb-10">
                    <button onclick="filterCategory('all')" class="cat-pill active px-4 py-2 rounded-lg text-sm font-medium bg-electric-500 text-white transition">All Tools</button>
                    <button onclick="filterCategory('text')" class="cat-pill px-4 py-2 rounded-lg text-sm font-medium bg-navy-800 text-gray-300 hover:bg-navy-700 transition">Text & Writing</button>
                    <button onclick="filterCategory('developer')" class="cat-pill px-4 py-2 rounded-lg text-sm font-medium bg-navy-800 text-gray-300 hover:bg-navy-700 transition">Developer Utilities</button>
                    <button onclick="filterCategory('math')" class="cat-pill px-4 py-2 rounded-lg text-sm font-medium bg-navy-800 text-gray-300 hover:bg-navy-700 transition">Calculators</button>
                    <button onclick="filterCategory('ai')" class="cat-pill px-4 py-2 rounded-lg text-sm font-medium bg-navy-800 text-gray-300 hover:bg-navy-700 transition">AI Assistants</button>
                </div>

                <!-- Tools Grid -->
                <div id="tools-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6"></div>
            </div>
        </div>

        <!-- DASHBOARD VIEW -->
        <div id="view-dashboard" class="view-section hidden py-16">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-8 pb-6 border-b border-gray-800">
                    <div>
                        <h1 class="text-2xl sm:text-3xl font-bold">User Workspace Dashboard</h1>
                        <p class="text-gray-400 text-sm mt-1">Manage your saved tools, session preferences, and administrative controls.</p>
                    </div>
                    <div class="mt-4 md:mt-0 flex items-center space-x-3">
                        <span id="user-role-badge" class="px-3 py-1 rounded-full bg-electric-500/20 text-electric-400 text-xs font-semibold border border-electric-500/30">Member Session</span>
                        <button onclick="toggleAdminRole()" class="px-3 py-1 rounded-lg bg-navy-800 border border-gray-700 text-xs font-medium hover:bg-navy-700 transition">Toggle Admin View</button>
                    </div>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                    <div class="bg-navy-800 border border-gray-700 rounded-2xl p-6 space-y-6">
                        <div class="flex items-center space-x-4">
                            <div class="w-14 h-14 rounded-2xl bg-gradient-to-tr from-electric-500 to-cyan-400 flex items-center justify-center text-xl font-bold text-white shadow-lg">HM</div>
                            <div>
                                <h3 class="font-bold text-white">Huzaifa Mansha</h3>
                                <p class="text-xs text-gray-400">huzaifa@nexora.workspace</p>
                            </div>
                        </div>
                        <div class="space-y-3 pt-4 border-t border-gray-700">
                            <div class="flex justify-between text-sm"><span class="text-gray-400">Account Tier</span><span class="font-semibold text-cyan-400">Pro Enterprise</span></div>
                            <div class="flex justify-between text-sm"><span class="text-gray-400">API Access</span><span class="font-semibold text-emerald-400">Enabled (BYOK)</span></div>
                            <div class="flex justify-between text-sm"><span class="text-gray-400">Saved Bookmarks</span><span id="saved-count" class="font-semibold text-white">4 Tools</span></div>
                        </div>
                    </div>

                    <div class="lg:col-span-2 space-y-8">
                        <div class="bg-navy-800 border border-gray-700 rounded-2xl p-6">
                            <h3 class="text-lg font-bold text-white mb-4"><i class="fa-solid fa-bookmark text-electric-400 mr-2"></i> Recent Bookmarked Tools</h3>
                            <div id="bookmarked-tools-list" class="grid grid-cols-1 sm:grid-cols-2 gap-4"></div>
                        </div>

                        <div id="admin-panel" class="hidden bg-navy-800 border border-amber-500/40 rounded-2xl p-6">
                            <div class="flex justify-between items-center mb-4">
                                <h3 class="text-lg font-bold text-amber-400"><i class="fa-solid fa-shield-halved mr-2"></i> Admin Content Management & Analytics</h3>
                                <span class="text-xs px-2.5 py-1 rounded bg-amber-500/10 text-amber-400 font-mono">CMS Active</span>
                            </div>
                            <p class="text-gray-300 text-sm mb-4">Publish blog announcements, review platform traffic telemetry, and export system compliance records.</p>
                            <div class="flex flex-wrap gap-3">
                                <button onclick="alert('Blog post published successfully!')" class="px-4 py-2 rounded-lg bg-amber-500 text-navy-900 text-sm font-semibold hover:bg-amber-400 transition">Publish New Article</button>
                                <button onclick="alert('System logs exported as JSON.')" class="px-4 py-2 rounded-lg bg-navy-700 border border-gray-600 text-sm font-medium text-gray-200 hover:bg-navy-600 transition">Export Audit Logs</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- BLOG & GUIDES VIEW -->
        <div id="view-blog" class="view-section hidden py-16">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-3xl mx-auto mb-16">
                    <h1 class="text-3xl sm:text-4xl font-bold">Blog, Guides & Tutorials</h1>
                    <p class="text-gray-400 mt-2">Expert insights on AI integration, frontend architecture, and modern productivity workflows.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <div class="bg-navy-800 border border-gray-700 rounded-2xl
 overflow-hidden hover:border-electric-500 transition">
                        <div class="h-48 bg-gradient-to-tr from-blue-900 to-indigo-900 flex items-center justify-center text-electric-400 text-3xl"><i class="fa-solid fa-brain"></i></div>
                        <div class="p-6">
                            <span class="text-xs font-semibold text-electric-400 uppercase tracking-wider">AI Integration</span>
                            <h3 class="text-xl font-bold t

# Nexora — AI & Productivity Hub

![Nexora Banner](assets/banner.png)

A professionally designed commercial SaaS platform built with modern Tailwind CSS, featuring a complete tools suite, user dashboard, admin CMS, and secure client-side utilities[span_4](start_span)[span_4](end_span).

## Publishing to GitHub & Vercel

### Option 1: GitHub Pages (Static Hosting)
1. Create a new public repository on GitHub (e.g. `nexora`)[span_5](start_span)[span_5](end_span).
2. Upload `index.html`, `.nojekyll`, and the `assets/` folder to the root of the repository[span_6](start_span)[span_6](end_span).
3. Go to **Settings > Pages**, select `main` branch root (`/`), and click Save[span_7](start_span)[span_7](end_span).
4. Your site will be live at `https://<username>.github.io/nexora/`[span_8](start_span)[span_8](end_span).

### Option 2: Vercel (Recommended for SaaS Apps)
1. Log in to [Vercel](https://vercel.com/) with GitHub[span_9](start_span)[span_9](end_span).
2. Click **Add New > Project** and import your `nexora` repository[span_10](start_span)[span_10](end_span).
3. Click **Deploy**. Vercel will instantly generate a secure live production URL[span_11](start_span)[span_11](end_span).

## Features
- **Phase 1:** Responsive midnight navy SaaS aesthetic, glassmorphism cards, pricing tables, FAQ, blog layouts[span_12](start_span)[span_12](end_span).
- **Phase 2:** Role-based authentication modal, user dashboard with bookmarking and Admin CMS mode[span_13](start_span)[span_13](end_span).
- **Phase 3:** 12 fully functional browser-side tools (Word Counter, QR Code Generator with PNG export, JSON Beautifier, Password Generator, Unit Converter, etc.)[span_14](start_span)[span_14](end_span).
- **Phase 4:** SEO metadata, Cookie consent notice, Privacy Policy & Terms of Service modals[span_15](start_span)[span_15](end_span).


