<!DOCTYPE html><html lang="en"><head>
    <meta charset="UTF-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>HouseFind Phoenix - Event Discovery Platform</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&amp;family=Playfair+Display:ital,wght@0,400;0,700;1,400&amp;display=swap" rel="stylesheet"/>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>
    <style>
        :root {
            --primary: #FF6B35;
            --primary-dark: #E85D2F;
            --secondary: #0F766E;
            --accent: #F59E0B;
            --neutral: #374151;
            --base-100: #ffffff;
            --base-200: #f9fafb;
            --base-300: #f3f4f6;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.7;
            color: var(--neutral);
        }
        
        .font-display {
            font-family: 'Playfair Display', serif;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .hero-overlay {
            background: linear-gradient(135deg, rgba(255, 107, 53, 0.1) 0%, rgba(15, 118, 110, 0.1) 100%);
        }
        
        .toc-fixed {
            position: fixed;
            top: 20px;
            left: 20px;
            width: 280px;
            max-height: calc(100vh - 40px);
            overflow-y: auto;
            z-index: 50;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border: 1px solid var(--base-300);
            border-radius: 12px;
            padding: 24px;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }
        
        .main-content {
            margin-left: 320px;
            max-width: 900px;
        }
        
        .metric-card {
            background: linear-gradient(135deg, var(--base-100) 0%, var(--base-200) 100%);
            border: 1px solid var(--base-300);
            transition: all 0.3s ease;
        }
        
        .metric-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
        }
        
        .status-badge {
            display: inline-flex;
            align-items: center;
            gap: 4px;
            padding: 4px 12px;
            border-radius: 9999px;
            font-size: 0.75rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }
        
        .status-excellent {
            background-color: #dcfce7;
            color: #166534;
        }
        
        .status-superior {
            background-color: #dbeafe;
            color: #1e40af;
        }
        
        .status-perfect {
            background-color: #fef3c7;
            color: #92400e;
        }
        
        .tech-stack-item {
            background: var(--base-100);
            border: 1px solid var(--base-300);
            border-radius: 8px;
            padding: 16px;
            transition: all 0.3s ease;
        }
        
        .tech-stack-item:hover {
            border-color: var(--primary);
            box-shadow: 0 4px 12px -2px rgba(255, 107, 53, 0.1);
        }
        
        .code-block {
            background: #1f2937;
            color: #e5e7eb;
            border-radius: 8px;
            padding: 20px;
            overflow-x: auto;
            font-family: 'Fira Code', monospace;
            font-size: 0.875rem;
            line-height: 1.6;
        }
        
        @media (max-width: 1024px) {
            .toc-fixed {
                display: none;
            }
            .main-content {
                margin-left: 0;
                padding: 0 20px;
            }
        }

        @media (max-width: 768px) {
            .grid.grid-cols-2 {
                grid-template-columns: 1fr;
            }
            .bento-grid {
                flex-direction: column;
            }
            .hero-overlay .container {
                padding-left: 1rem;
                padding-right: 1rem;
            }
        }
    </style>
  </head>

  <body class="bg-gray-50">
    <!-- Fixed Table of Contents -->
    <div class="toc-fixed">
      <h3 class="font-display font-bold text-lg mb-4 gradient-text">Contents</h3>
      <nav class="space-y-2">
        <a href="#hero" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">Hero &amp; Overview</a>
        <a href="#metrics" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">Performance Metrics</a>
        <a href="#security" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">Security Features</a>
        <a href="#features" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">Production Features</a>
        <a href="#tech-stack" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">Technology Stack</a>
        <a href="#performance" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">Performance Optimizations</a>
        <a href="#installation" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">Installation &amp; Setup</a>
        <a href="#deployment" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">Production Deployment</a>
        <a href="#api" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">API Endpoints</a>
        <a href="#monitoring" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">Monitoring &amp; Analytics</a>
        <a href="#community" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">Phoenix Music Scene</a>
        <a href="#contributing" class="block text-sm text-gray-600 hover:text-orange-500 transition-colors">Contributing</a>
      </nav>
    </div>

    <!-- Main Content -->
    <div class="main-content">
      <!-- Hero Section -->
      <section id="hero" class="mb-16">
        <div class="hero-overlay rounded-2xl p-6 md:p-12 mb-8">
          <div class="bento-grid flex gap-6 items-center">
            <div class="flex-1">
              <img src="https://kimi-web-img.moonshot.cn/img/images.squarespace-cdn.com/a29ad4ec734052f34f06ceb596c9607434c416f2.jpg" alt="Phoenix desert sunset landscape" class="w-full h-80 object-cover rounded-xl shadow-lg" size="large" aspect="wide" style="photo" query="phoenix desert sunset landscape" referrerpolicy="no-referrer" data-modified="1" data-score="0.00"/>
            </div>
            <div class="flex-1">
              <div class="mb-6">
                <span class="inline-flex items-center px-3 py-1 rounded-full text-sm font-medium bg-orange-100 text-orange-800">
                  <i class="fas fa-music mr-2"></i>
                  Event Discovery Platform
                </span>
              </div>
              <h1 class="font-display text-4xl md:text-5xl font-bold mb-4 gradient-text italic">
                HouseFind Phoenix
              </h1>
              <p class="text-xl text-gray-700 mb-6 leading-relaxed">
                A production-ready event discovery platform for Phoenix&#39;s underground electronic music scene.
                Built with industry standards, security-first architecture, and real-time performance monitoring.
              </p>
              <div class="flex flex-wrap gap-3">
                <a href="#features" class="inline-flex items-center px-4 py-2 bg-orange-500 text-white rounded-lg hover:bg-orange-600 transition-colors">
                  <i class="fas fa-rocket mr-2"></i>
                  Explore Features
                </a>
                <a href="#tech-stack" class="inline-flex items-center px-4 py-2 border border-gray-300 text-gray-700 rounded-lg hover:border-orange-500 hover:text-orange-500 transition-colors">
                  <i class="fas fa-code mr-2"></i>
                  View Tech Stack
                </a>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Key Metrics Overview -->
      <section id="metrics" class="mb-16">
        <h2 class="font-display text-3xl font-bold mb-8 text-gray-900">Performance Excellence</h2>

        <div class="grid md:grid-cols-2 gap-6 mb-8">
          <div class="metric-card rounded-xl p-6">
            <div class="flex items-center justify-between mb-4">
              <h3 class="font-semibold text-gray-900">API Response Time</h3>
              <span class="status-badge status-excellent">
                <i class="fas fa-check-circle"></i>
                Exceeded
              </span>
            </div>
            <div class="text-3xl font-bold text-orange-500 mb-2">71-752ms</div>
            <p class="text-gray-600">Well under industry standard of &lt;1 second</p>
          </div>

          <div class="metric-card rounded-xl p-6">
            <div class="flex items-center justify-between mb-4">
              <h3 class="font-semibold text-gray-900">Database Queries</h3>
              <span class="status-badge status-excellent">
                <i class="fas fa-check-circle"></i>
                Exceeded
              </span>
            </div>
            <div class="text-3xl font-bold text-teal-600 mb-2">145-220ms</div>
            <p class="text-gray-600">Optimized queries under 500ms standard</p>
          </div>

          <div class="metric-card rounded-xl p-6">
            <div class="flex items-center justify-between mb-4">
              <h3 class="font-semibold text-gray-900">Cache Performance</h3>
              <span class="status-badge status-excellent">
                <i class="fas fa-star"></i>
                Excellent
              </span>
            </div>
            <div class="text-3xl font-bold text-amber-500 mb-2">9x</div>
            <p class="text-gray-600">Performance improvement vs 2-3x standard</p>
          </div>

          <div class="metric-card rounded-xl p-6">
            <div class="flex items-center justify-between mb-4">
              <h3 class="font-semibold text-gray-900">Security Score</h3>
              <span class="status-badge status-perfect">
                <i class="fas fa-shield-alt"></i>
                Perfect
              </span>
            </div>
            <div class="text-3xl font-bold text-amber-600 mb-2">100%</div>
            <p class="text-gray-600">Zero vulnerabilities detected</p>
          </div>
        </div>

        <div class="bg-white rounded-xl p-6 border border-gray-200">
          <h3 class="font-semibold text-gray-900 mb-4">Complete Performance Metrics</h3>
          <div class="overflow-x-auto">
            <table class="w-full text-sm">
              <thead>
                <tr class="border-b border-gray-200">
                  <th class="text-left py-3 font-semibold text-gray-900">Metric</th>
                  <th class="text-left py-3 font-semibold text-gray-900">Industry Standard</th>
                  <th class="text-left py-3 font-semibold text-gray-900">HouseFind Phoenix</th>
                  <th class="text-left py-3 font-semibold text-gray-900">Status</th>
                </tr>
              </thead>
              <tbody class="divide-y divide-gray-100">
                <tr>
                  <td class="py-3 font-medium">API Response Time</td>
                  <td class="py-3 text-gray-600">&lt; 1 second</td>
                  <td class="py-3 font-semibold text-orange-500">71-752ms</td>
                  <td class="py-3">
                    <span class="status-badge status-excellent">
                      <i class="fas fa-check-circle"></i>
                      Exceeded
                    </span>
                  </td>
                </tr>
                <tr>
                  <td class="py-3 font-medium">Database Queries</td>
                  <td class="py-3 text-gray-600">&lt; 500ms</td>
                  <td class="py-3 font-semibold text-teal-600">145-220ms</td>
                  <td class="py-3">
                    <span class="status-badge status-excellent">
                      <i class="fas fa-check-circle"></i>
                      Exceeded
                    </span>
                  </td>
                </tr>
                <tr>
                  <td class="py-3 font-medium">Cache Performance</td>
                  <td class="py-3 text-gray-600">2-3x improvement</td>
                  <td class="py-3 font-semibold text-amber-500">9x improvement</td>
                  <td class="py-3">
                    <span class="status-badge status-excellent">
                      <i class="fas fa-star"></i>
                      Excellent
                    </span>
                  </td>
                </tr>
                <tr>
                  <td class="py-3 font-medium">Page Load Time</td>
                  <td class="py-3 text-gray-600">&lt; 3 seconds</td>
                  <td class="py-3 font-semibold text-blue-600">&lt; 1 second</td>
                  <td class="py-3">
                    <span class="status-badge status-superior">
                      <i class="fas fa-rocket"></i>
                      Superior
                    </span>
                  </td>
                </tr>
                <tr>
                  <td class="py-3 font-medium">Security Score</td>
                  <td class="py-3 text-gray-600">80%+</td>
                  <td class="py-3 font-semibold text-amber-600">100%</td>
                  <td class="py-3">
                    <span class="status-badge status-perfect">
                      <i class="fas fa-shield-alt"></i>
                      Perfect
                    </span>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </section>

      <!-- Security Features -->
      <section id="security" class="mb-16">
        <h2 class="font-display text-3xl font-bold mb-8 text-gray-900">Enterprise-Grade Security</h2>

        <div class="grid md:grid-cols-3 gap-6 mb-8">
          <div class="bg-white rounded-xl p-6 border border-gray-200">
            <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center mb-4">
              <i class="fas fa-shield-alt text-green-600 text-xl"></i>
            </div>
            <h3 class="font-semibold text-gray-900 mb-3">Zero Vulnerabilities</h3>
            <p class="text-gray-600 text-sm">No security vulnerabilities detected by industry-standard scanners</p>
          </div>

          <div class="bg-white rounded-xl p-6 border border-gray-200">
            <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-4">
              <i class="fas fa-lock text-blue-600 text-xl"></i>
            </div>
            <h3 class="font-semibold text-gray-900 mb-3">CSRF Protection</h3>
            <p class="text-gray-600 text-sm">Comprehensive CSRF protection on all state-changing endpoints</p>
          </div>

          <div class="bg-white rounded-xl p-6 border border-gray-200">
            <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mb-4">
              <i class="fas fa-database text-purple-600 text-xl"></i>
            </div>
            <h3 class="font-semibold text-gray-900 mb-3">SQL Injection Prevention</h3>
            <p class="text-gray-600 text-sm">Parameterized queries eliminate SQL injection risks</p>
          </div>
        </div>

        <div class="space-y-4">
          <h3 class="font-semibold text-gray-900">Comprehensive Security Measures</h3>
          <ul class="space-y-2">
            <li class="flex items-start gap-3">
              <i class="fas fa-check-circle text-green-500 mt-1"></i>
              <span class="text-gray-700"><strong>Environment Variable Security:</strong> No hardcoded secrets, all configuration through secure environment variables</span>
            </li>
            <li class="flex items-start gap-3">
              <i class="fas fa-check-circle text-green-500 mt-1"></i>
              <span class="text-gray-700"><strong>Rate Limiting:</strong> Tiered protection strategies prevent abuse and ensure fair usage</span>
            </li>
            <li class="flex items-start gap-3">
              <i class="fas fa-check-circle text-green-500 mt-1"></i>
              <span class="text-gray-700"><strong>Input Validation:</strong> Comprehensive Zod schemas validate all incoming data</span>
            </li>
          </ul>
        </div>
      </section>

      <!-- Production Features -->
      <section id="features" class="mb-16">
        <h2 class="font-display text-3xl font-bold mb-8 text-gray-900">Production-Ready Features</h2>

        <div class="space-y-8">
          <div>
            <h3 class="font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <i class="fas fa-calendar-alt text-orange-500"></i>
              Real Phoenix Music Scene Data
            </h3>
            <div class="grid md:grid-cols-3 gap-4">
              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <div class="text-2xl font-bold text-orange-500 mb-1">13</div>
                <div class="text-sm text-gray-600">Active Events</div>
              </div>
              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <div class="text-2xl font-bold text-teal-600 mb-1">3</div>
                <div class="text-sm text-gray-600">Verified Venues</div>
              </div>
              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <div class="text-2xl font-bold text-amber-500 mb-1">3</div>
                <div class="text-sm text-gray-600">Event Sources</div>
              </div>
            </div>
            <p class="text-gray-700 mt-4">
              Comprehensive event coverage from multiple sources including user submissions, 19hz data, and verified venue partnerships.
            </p>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <i class="fas fa-filter text-teal-600"></i>
              Advanced Filtering System
            </h3>
            <div class="grid md:grid-cols-2 gap-4">
              <div class="space-y-2">
                <div class="flex items-center gap-2 text-sm">
                  <i class="fas fa-music text-gray-500"></i>
                  <span>Multi-genre filtering (House, Techno, Afro House, Minimal)</span>
                </div>
                <div class="flex items-center gap-2 text-sm">
                  <i class="fas fa-map-marker-alt text-gray-500"></i>
                  <span>Multi-venue selection with map integration</span>
                </div>
                <div class="flex items-center gap-2 text-sm">
                  <i class="fas fa-calendar text-gray-500"></i>
                  <span>Date range filters (Today, Week, Month, Custom)</span>
                </div>
              </div>
              <div class="space-y-2">
                <div class="flex items-center gap-2 text-sm">
                  <i class="fas fa-dollar-sign text-gray-500"></i>
                  <span>Price range filtering with min/max controls</span>
                </div>
                <div class="flex items-center gap-2 text-sm">
                  <i class="fas fa-upload text-gray-500"></i>
                  <span>Source filtering (User submitted, Scraped, Verified)</span>
                </div>
                <div class="flex items-center gap-2 text-sm">
                  <i class="fas fa-crosshairs text-gray-500"></i>
                  <span>Location-based search with radius filtering</span>
                </div>
              </div>
            </div>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <i class="fas fa-mobile-alt text-blue-600"></i>
              Professional User Experience
            </h3>
            <div class="space-y-3">
              <div class="flex items-center gap-3">
                <span class="px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm font-medium">Responsive Design</span>
                <span class="text-gray-600">Optimized for mobile devices with PWA capabilities</span>
              </div>
              <div class="flex items-center gap-3">
                <span class="px-3 py-1 bg-green-100 text-green-800 rounded-full text-sm font-medium">Real-time Updates</span>
                <span class="text-gray-600">Server-Sent Events for live event updates</span>
              </div>
              <div class="flex items-center gap-3">
                <span class="px-3 py-1 bg-purple-100 text-purple-800 rounded-full text-sm font-medium">Accessibility</span>
                <span class="text-gray-600">ARIA-compliant components for inclusive design</span>
              </div>
              <div class="flex items-center gap-3">
                <span class="px-3 py-1 bg-gray-800 text-white rounded-full text-sm font-medium">Dark Theme</span>
                <span class="text-gray-600">Optimized for nighttime use with performance monitoring</span>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Technology Stack -->
      <section id="tech-stack" class="mb-16">
        <h2 class="font-display text-3xl font-bold mb-8 text-gray-900">Technology Stack</h2>

        <div class="space-y-8">
          <div>
            <h3 class="font-semibold text-gray-900 mb-4">Frontend (Industry Standard)</h3>
            <div class="grid md:grid-cols-2 gap-4">
              <div class="tech-stack-item">
                <div class="flex items-start justify-between mb-2">
                  <div>
                    <h4 class="font-semibold text-gray-900">React 18</h4>
                    <p class="text-sm text-gray-600">with TypeScript</p>
                  </div>
                  <i class="fab fa-react text-blue-500 text-2xl"></i>
                </div>
                <div class="flex flex-wrap gap-1 mt-2">
                  <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded text-xs">Component-based</span>
                  <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs">Type-safe</span>
                </div>
              </div>

              <div class="tech-stack-item">
                <div class="flex items-start justify-between mb-2">
                  <div>
                    <h4 class="font-semibold text-gray-900">Vite</h4>
                    <p class="text-sm text-gray-600">Blazing fast builds</p>
                  </div>
                  <i class="fas fa-bolt text-yellow-500 text-2xl"></i>
                </div>
                <div class="flex flex-wrap gap-1 mt-2">
                  <span class="px-2 py-1 bg-yellow-100 text-yellow-800 rounded text-xs">Fast HMR</span>
                  <span class="px-2 py-1 bg-orange-100 text-orange-800 rounded text-xs">Optimized</span>
                </div>
              </div>

              <div class="tech-stack-item">
                <div class="flex items-start justify-between mb-2">
                  <div>
                    <h4 class="font-semibold text-gray-900">TanStack Query v5</h4>
                    <p class="text-sm text-gray-600">Server state management</p>
                  </div>
                  <i class="fas fa-sync-alt text-purple-500 text-2xl"></i>
                </div>
                <div class="flex flex-wrap gap-1 mt-2">
                  <span class="px-2 py-1 bg-purple-100 text-purple-800 rounded text-xs">Caching</span>
                  <span class="px-2 py-1 bg-indigo-100 text-indigo-800 rounded text-xs">Auto-refetch</span>
                </div>
              </div>

              <div class="tech-stack-item">
                <div class="flex items-start justify-between mb-2">
                  <div>
                    <h4 class="font-semibold text-gray-900">Tailwind CSS</h4>
                    <p class="text-sm text-gray-600">Responsive styling</p>
                  </div>
                  <i class="fas fa-paint-brush text-cyan-500 text-2xl"></i>
                </div>
                <div class="flex flex-wrap gap-1 mt-2">
                  <span class="px-2 py-1 bg-cyan-100 text-cyan-800 rounded text-xs">Utility-first</span>
                  <span class="px-2 py-1 bg-teal-100 text-teal-800 rounded text-xs">Responsive</span>
                </div>
              </div>
            </div>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4">Backend (Enterprise-Grade)</h3>
            <div class="grid md:grid-cols-2 gap-4">
              <div class="tech-stack-item">
                <div class="flex items-start justify-between mb-2">
                  <div>
                    <h4 class="font-semibold text-gray-900">Node.js + Express</h4>
                    <p class="text-sm text-gray-600">TypeScript backend</p>
                  </div>
                  <i class="fab fa-node-js text-green-600 text-2xl"></i>
                </div>
                <div class="flex flex-wrap gap-1 mt-2">
                  <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs">Scalable</span>
                  <span class="px-2 py-1 bg-gray-100 text-gray-800 rounded text-xs">Type-safe</span>
                </div>
              </div>

              <div class="tech-stack-item">
                <div class="flex items-start justify-between mb-2">
                  <div>
                    <h4 class="font-semibold text-gray-900">PostgreSQL</h4>
                    <p class="text-sm text-gray-600">Neon serverless</p>
                  </div>
                  <i class="fas fa-database text-blue-600 text-2xl"></i>
                </div>
                <div class="flex flex-wrap gap-1 mt-2">
                  <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded text-xs">Relational</span>
                  <span class="px-2 py-1 bg-indigo-100 text-indigo-800 rounded text-xs">Serverless</span>
                </div>
              </div>

              <div class="tech-stack-item">
                <div class="flex items-start justify-between mb-2">
                  <div>
                    <h4 class="font-semibold text-gray-900">Drizzle ORM</h4>
                    <p class="text-sm text-gray-600">Type-safe queries</p>
                  </div>
                  <i class="fas fa-layer-group text-orange-600 text-2xl"></i>
                </div>
                <div class="flex flex-wrap gap-1 mt-2">
                  <span class="px-2 py-1 bg-orange-100 text-orange-800 rounded text-xs">Type-safe</span>
                  <span class="px-2 py-1 bg-red-100 text-red-800 rounded text-xs">Performant</span>
                </div>
              </div>

              <div class="tech-stack-item">
                <div class="flex items-start justify-between mb-2">
                  <div>
                    <h4 class="font-semibold text-gray-900">Session-based Auth</h4>
                    <p class="text-sm text-gray-600">bcrypt hashing</p>
                  </div>
                  <i class="fas fa-key text-purple-600 text-2xl"></i>
                </div>
                <div class="flex flex-wrap gap-1 mt-2">
                  <span class="px-2 py-1 bg-purple-100 text-purple-800 rounded text-xs">Secure</span>
                  <span class="px-2 py-1 bg-pink-100 text-pink-800 rounded text-xs">Encrypted</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Performance Optimizations -->
      <section id="performance" class="mb-16">
        <h2 class="font-display text-3xl font-bold mb-8 text-gray-900">Performance Optimizations</h2>

        <div class="grid md:grid-cols-2 gap-8">
          <div>
            <h3 class="font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <i class="fas fa-database text-blue-600"></i>
              Database Strategy
            </h3>
            <div class="space-y-4">
              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <h4 class="font-medium text-gray-900 mb-2">31+ Strategic Indexes</h4>
                <p class="text-gray-600 text-sm mb-2">Carefully crafted indexes optimize query performance across all major access patterns.</p>
                <div class="flex items-center gap-2 text-sm text-green-600">
                  <i class="fas fa-chart-line"></i>
                  <span>Query times consistently under 250ms</span>
                </div>
              </div>

              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <h4 class="font-medium text-gray-900 mb-2">Cursor-based Pagination</h4>
                <p class="text-gray-600 text-sm mb-2">Replaces slow OFFSET queries with efficient cursor-based navigation.</p>
                <div class="flex items-center gap-2 text-sm text-blue-600">
                  <i class="fas fa-arrow-right"></i>
                  <span>Eliminates performance degradation</span>
                </div>
              </div>

              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <h4 class="font-medium text-gray-900 mb-2">Optimized JOIN Operations</h4>
                <p class="text-gray-600 text-sm mb-2">Eliminates N+1 queries through strategic query planning and eager loading.</p>
                <div class="flex items-center gap-2 text-sm text-purple-600">
                  <i class="fas fa-link"></i>
                  <span>Efficient relationship fetching</span>
                </div>
              </div>
            </div>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <i class="fas fa-memory text-orange-600"></i>
              Caching Architecture
            </h3>
            <div class="space-y-4">
              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <h4 class="font-medium text-gray-900 mb-2">Server-side LRU Cache</h4>
                <p class="text-gray-600 text-sm mb-2">In-memory cache with 45-second TTL for frequently accessed data.</p>
                <div class="flex items-center gap-2 text-sm text-orange-600">
                  <i class="fas fa-tachometer-alt"></i>
                  <span>9x performance improvement</span>
                </div>
              </div>

              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <h4 class="font-medium text-gray-900 mb-2">Client-side Query Caching</h4>
                <p class="text-gray-600 text-sm mb-2">TanStack Query intelligent caching with automatic background refetching.</p>
                <div class="flex items-center gap-2 text-sm text-teal-600">
                  <i class="fas fa-sync"></i>
                  <span>Stale-while-revalidate pattern</span>
                </div>
              </div>

              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <h4 class="font-medium text-gray-900 mb-2">Strategic Cache Invalidation</h4>
                <p class="text-gray-600 text-sm mb-2">Smart invalidation patterns ensure data consistency across all layers.</p>
                <div class="flex items-center gap-2 text-sm text-green-600">
                  <i class="fas fa-brain"></i>
                  <span>Intelligent cache management</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Installation &amp; Setup -->
      <section id="installation" class="mb-16">
        <h2 class="font-display text-3xl font-bold mb-8 text-gray-900">Installation &amp; Setup</h2>

        <div class="space-y-8">
          <div>
            <h3 class="font-semibold text-gray-900 mb-4">Prerequisites</h3>
            <ul class="space-y-2">
              <li class="flex items-center gap-3">
                <i class="fab fa-node-js text-green-600"></i>
                <span class="text-gray-700">Node.js 18+</span>
              </li>
              <li class="flex items-center gap-3">
                <i class="fas fa-database text-blue-600"></i>
                <span class="text-gray-700">PostgreSQL database</span>
              </li>
              <li class="flex items-center gap-3">
                <i class="fas fa-cog text-gray-600"></i>
                <span class="text-gray-700">Environment variables configured</span>
              </li>
            </ul>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4">Quick Start</h3>
            <div class="code-block">
              <div class="mb-4">
                <div class="text-gray-400 text-sm mb-2"># Install dependencies</div>
                <div>npm install</div>
              </div>
              <div class="mb-4">
                <div class="text-gray-400 text-sm mb-2"># Set up environment variables</div>
                <div>cp .env.example .env</div>
                <div class="text-gray-400 text-sm mt-1"># Edit .env with your configuration</div>
              </div>
              <div class="mb-4">
                <div class="text-gray-400 text-sm mb-2"># Run database migrations</div>
                <div>npm run db:push</div>
              </div>
              <div>
                <div class="text-gray-400 text-sm mb-2"># Start development server</div>
                <div>npm run dev</div>
              </div>
            </div>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4">Environment Variables</h3>
            <div class="bg-yellow-50 border border-yellow-200 rounded-lg p-4 mb-4">
              <p class="text-yellow-800 text-sm flex items-center gap-2">
                <i class="fas fa-exclamation-triangle"></i>
                <span>Required for production deployment</span>
              </p>
            </div>
            <div class="code-block">
              <div class="mb-3">
                <div class="text-gray-400 text-sm mb-2"># Database</div>
                <div>DATABASE_URL=postgresql://...</div>
              </div>
              <div class="mb-3">
                <div class="text-gray-400 text-sm mb-2"># Security</div>
                <div>SESSION_SECRET=your-secure-secret</div>
              </div>
              <div class="mb-3">
                <div class="text-gray-400 text-sm mb-2"># Supabase (if using auth features)</div>
                <div>VITE_SUPABASE_URL=https://your-project.supabase.co</div>
                <div>VITE_SUPABASE_ANON_KEY=your-anon-key</div>
              </div>
              <div>
                <div class="text-gray-400 text-sm mb-2"># Optional OAuth</div>
                <div>SOUNDCLOUD_CLIENT_ID=...</div>
                <div>SPOTIFY_CLIENT_ID=...</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Production Deployment -->
      <section id="deployment" class="mb-16">
        <h2 class="font-display text-3xl font-bold mb-8 text-gray-900">Production Deployment</h2>

        <div class="space-y-8">
          <div>
            <h3 class="font-semibold text-gray-900 mb-4">Pre-Deployment Checklist</h3>
            <div class="grid md:grid-cols-2 gap-4">
              <div class="space-y-3">
                <div class="flex items-center gap-3">
                  <i class="fas fa-check-circle text-green-500"></i>
                  <span class="text-gray-700">Set all required environment variables</span>
                </div>
                <div class="flex items-center gap-3">
                  <i class="fas fa-check-circle text-green-500"></i>
                  <span class="text-gray-700">Enable HTTPS/TLS</span>
                </div>
                <div class="flex items-center gap-3">
                  <i class="fas fa-check-circle text-green-500"></i>
                  <span class="text-gray-700">Configure CORS for your domain</span>
                </div>
              </div>
              <div class="space-y-3">
                <div class="flex items-center gap-3">
                  <i class="fas fa-check-circle text-green-500"></i>
                  <span class="text-gray-700">Set up database backups</span>
                </div>
                <div class="flex items-center gap-3">
                  <i class="fas fa-check-circle text-green-500"></i>
                  <span class="text-gray-700">Configure monitoring/alerting</span>
                </div>
                <div class="flex items-center gap-3">
                  <i class="fas fa-check-circle text-green-500"></i>
                  <span class="text-gray-700">Review rate limiting settings</span>
                </div>
              </div>
            </div>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4">Deployment Steps</h3>
            <div class="code-block mb-4">
              <div class="mb-4">
                <div class="text-gray-400 text-sm mb-2"># Build for production:</div>
                <div>npm run build</div>
              </div>
              <div class="mb-4">
                <div class="text-gray-400 text-sm mb-2"># Run production server:</div>
                <div>NODE_ENV=production npm start</div>
              </div>
            </div>

            <div class="bg-blue-50 border border-blue-200 rounded-lg p-4">
              <h4 class="font-medium text-blue-900 mb-2">Health Monitoring Endpoints</h4>
              <ul class="space-y-1 text-sm text-blue-800">
                <li>• API Health: <code class="bg-blue-100 px-2 py-1 rounded">GET /api/health</code></li>
                <li>• Database Status: <code class="bg-blue-100 px-2 py-1 rounded">GET /api/health/db</code></li>
                <li>• Background Jobs: Check logs for service status</li>
              </ul>
            </div>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4">Performance Monitoring</h3>
            <p class="text-gray-700 mb-4">
              The application includes built-in performance tracking to help you monitor and optimize your deployment:
            </p>
            <ul class="space-y-2">
              <li class="flex items-start gap-3">
                <i class="fas fa-clock text-orange-500 mt-1"></i>
                <span class="text-gray-700">Query execution times in API responses</span>
              </li>
              <li class="flex items-start gap-3">
                <i class="fas fa-chart-bar text-blue-500 mt-1"></i>
                <span class="text-gray-700">Cache hit/miss rates via X-Cache headers</span>
              </li>
              <li class="flex items-start gap-3">
                <i class="fas fa-file-alt text-green-500 mt-1"></i>
                <span class="text-gray-700">Background job execution logs</span>
              </li>
              <li class="flex items-start gap-3">
                <i class="fas fa-bug text-red-500 mt-1"></i>
                <span class="text-gray-700">Error tracking capabilities</span>
              </li>
            </ul>
          </div>
        </div>
      </section>

      <!-- API Endpoints -->
      <section id="api" class="mb-16">
        <h2 class="font-display text-3xl font-bold mb-8 text-gray-900">API Endpoints</h2>

        <div class="space-y-8">
          <div>
            <h3 class="font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <i class="fas fa-calendar text-orange-500"></i>
              Events
            </h3>
            <div class="bg-white rounded-lg border border-gray-200 p-4 space-y-3">
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs font-medium">GET</span>
                <div>
                  <code class="text-sm font-medium">/api/events</code>
                  <p class="text-gray-600 text-sm mt-1">List events with comprehensive filtering options</p>
                </div>
              </div>
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs font-medium">GET</span>
                <div>
                  <code class="text-sm font-medium">/api/events/:id</code>
                  <p class="text-gray-600 text-sm mt-1">Get detailed information for a specific event</p>
                </div>
              </div>
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded text-xs font-medium">POST</span>
                <div>
                  <code class="text-sm font-medium">/api/events</code>
                  <p class="text-gray-600 text-sm mt-1">Submit new event (authentication required)</p>
                </div>
              </div>
            </div>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <i class="fas fa-user-music text-purple-500"></i>
              Artists
            </h3>
            <div class="bg-white rounded-lg border border-gray-200 p-4 space-y-3">
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs font-medium">GET</span>
                <div>
                  <code class="text-sm font-medium">/api/artists</code>
                  <p class="text-gray-600 text-sm mt-1">Browse and search artists</p>
                </div>
              </div>
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs font-medium">GET</span>
                <div>
                  <code class="text-sm font-medium">/api/artists/:id</code>
                  <p class="text-gray-600 text-sm mt-1">Get detailed artist profile</p>
                </div>
              </div>
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs font-medium">GET</span>
                <div>
                  <code class="text-sm font-medium">/api/artists/:id/events</code>
                  <p class="text-gray-600 text-sm mt-1">Get all events for a specific artist</p>
                </div>
              </div>
            </div>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <i class="fas fa-building text-blue-500"></i>
              Venues
            </h3>
            <div class="bg-white rounded-lg border border-gray-200 p-4 space-y-3">
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs font-medium">GET</span>
                <div>
                  <code class="text-sm font-medium">/api/venues</code>
                  <p class="text-gray-600 text-sm mt-1">List all venues with filtering</p>
                </div>
              </div>
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs font-medium">GET</span>
                <div>
                  <code class="text-sm font-medium">/api/venues/:id</code>
                  <p class="text-gray-600 text-sm mt-1">Get detailed venue information</p>
                </div>
              </div>
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs font-medium">GET</span>
                <div>
                  <code class="text-sm font-medium">/api/venues/:id/events</code>
                  <p class="text-gray-600 text-sm mt-1">Get all events at a specific venue</p>
                </div>
              </div>
            </div>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <i class="fas fa-lock text-red-500"></i>
              Authentication
            </h3>
            <div class="bg-white rounded-lg border border-gray-200 p-4 space-y-3">
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded text-xs font-medium">POST</span>
                <div>
                  <code class="text-sm font-medium">/api/auth/register</code>
                  <p class="text-gray-600 text-sm mt-1">User registration with email verification</p>
                </div>
              </div>
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded text-xs font-medium">POST</span>
                <div>
                  <code class="text-sm font-medium">/api/auth/login</code>
                  <p class="text-gray-600 text-sm mt-1">User login with session management</p>
                </div>
              </div>
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-red-100 text-red-800 rounded text-xs font-medium">POST</span>
                <div>
                  <code class="text-sm font-medium">/api/auth/logout</code>
                  <p class="text-gray-600 text-sm mt-1">User logout with session destruction</p>
                </div>
              </div>
              <div class="flex items-start gap-3">
                <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs font-medium">GET</span>
                <div>
                  <code class="text-sm font-medium">/api/auth/me</code>
                  <p class="text-gray-600 text-sm mt-1">Get current authenticated user</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Monitoring &amp; Analytics -->
      <section id="monitoring" class="mb-16">
        <h2 class="font-display text-3xl font-bold mb-8 text-gray-900">Monitoring &amp; Analytics</h2>

        <div class="space-y-8">
          <div>
            <h3 class="font-semibold text-gray-900 mb-4">Built-in Metrics</h3>
            <div class="grid md:grid-cols-2 gap-4">
              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <div class="flex items-center gap-3 mb-3">
                  <i class="fas fa-tachometer-alt text-orange-500 text-xl"></i>
                  <h4 class="font-medium text-gray-900">API Response Times</h4>
                </div>
                <p class="text-gray-600 text-sm">Real-time tracking of endpoint performance with percentile breakdowns</p>
              </div>

              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <div class="flex items-center gap-3 mb-3">
                  <i class="fas fa-database text-blue-500 text-xl"></i>
                  <h4 class="font-medium text-gray-900">Database Query Performance</h4>
                </div>
                <p class="text-gray-600 text-sm">Detailed query analysis with slow query detection and optimization suggestions</p>
              </div>

              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <div class="flex items-center gap-3 mb-3">
                  <i class="fas fa-memory text-purple-500 text-xl"></i>
                  <h4 class="font-medium text-gray-900">Cache Hit/Miss Rates</h4>
                </div>
                <p class="text-gray-600 text-sm">Monitor cache efficiency with real-time hit/miss ratio tracking</p>
              </div>

              <div class="bg-white rounded-lg p-4 border border-gray-200">
                <div class="flex items-center gap-3 mb-3">
                  <i class="fas fa-exclamation-triangle text-red-500 text-xl"></i>
                  <h4 class="font-medium text-gray-900">Error Rates by Endpoint</h4>
                </div>
                <p class="text-gray-600 text-sm">Track error frequencies and patterns across all API endpoints</p>
              </div>
            </div>
          </div>

          <div>
            <h3 class="font-semibold text-gray-900 mb-4">Recommended Monitoring Stack</h3>
            <div class="space-y-4">
              <div class="flex items-start gap-4 bg-white rounded-lg p-4 border border-gray-200">
                <div class="w-12 h-12 bg-red-100 rounded-lg flex items-center justify-center flex-shrink-0">
                  <i class="fas fa-bug text-red-600 text-xl"></i>
                </div>
                <div>
                  <h4 class="font-medium text-gray-900 mb-1">Application Monitoring</h4>
                  <p class="text-gray-600 text-sm mb-2">Sentry or DataDog for comprehensive error tracking and performance monitoring</p>
                  <div class="flex gap-2">
                    <span class="px-2 py-1 bg-red-100 text-red-800 rounded text-xs">Error Tracking</span>
                    <span class="px-2 py-1 bg-orange-100 text-orange-800 rounded text-xs">Performance</span>
                  </div>
                </div>
              </div>

              <div class="flex items-start gap-4 bg-white rounded-lg p-4 border border-gray-200">
                <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center flex-shrink-0">
                  <i class="fas fa-database text-blue-600 text-xl"></i>
                </div>
                <div>
                  <h4 class="font-medium text-gray-900 mb-1">Database Monitoring</h4>
                  <p class="text-gray-600 text-sm mb-2">pg_stat_statements for detailed query analysis and performance insights</p>
                  <div class="flex gap-2">
                    <span class="px-2 py-1 bg-blue-100 text-blue-800 rounded text-xs">Query Analysis</span>
                    <span class="px-2 py-1 bg-indigo-100 text-indigo-800 rounded text-xs">Performance</span>
                  </div>
                </div>
              </div>

              <div class="flex items-start gap-4 bg-white rounded-lg p-4 border border-gray-200">
                <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center flex-shrink-0">
                  <i class="fas fa-heartbeat text-green-600 text-xl"></i>
                </div>
                <div>
                  <h4 class="font-medium text-gray-900 mb-1">Uptime Monitoring</h4>
                  <p class="text-gray-600 text-sm mb-2">UptimeRobot or similar service for availability monitoring and alerts</p>
                  <div class="flex gap-2">
                    <span class="px-2 py-1 bg-green-100 text-green-800 rounded text-xs">Availability</span>
                    <span class="px-2 py-1 bg-teal-100 text-teal-800 rounded text-xs">Alerts</span>
                  </div>
                </div>
              </div>

              <div class="flex items-start gap-4 bg-white rounded-lg p-4 border border-gray-200">
                <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center flex-shrink-0">
                  <i class="fas fa-file-alt text-purple-600 text-xl"></i>
                </div>
                <div>
                  <h4 class="font-medium text-gray-900 mb-1">Log Aggregation</h4>
                  <p class="text-gray-600 text-sm mb-2">CloudWatch or Datadog for centralized log management and analysis</p>
                  <div class="flex gap-2">
                    <span class="px-2 py-1 bg-purple-100 text-purple-800 rounded text-xs">Centralized</span>
                    <span class="px-2 py-1 bg-pink-100 text-pink-800 rounded text-xs">Analysis</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Phoenix Music Scene -->
      <section id="community" class="mb-16">
        <h2 class="font-display text-3xl font-bold mb-8 text-gray-900">Phoenix&#39;s Underground Music Scene</h2>

        <div class="grid md:grid-cols-2 gap-8 mb-8">
          <div>
            <img src="https://kimi-web-img.moonshot.cn/img/blogger.googleusercontent.com/7951d676696d756afb5e123b968d417b1d649a2e.gif" alt="Phoenix underground electronic music event with desert-inspired lighting" class="w-full h-64 object-cover rounded-xl shadow-lg mb-6" size="medium" aspect="wide" style="photo" query="Phoenix underground electronic music event" referrerpolicy="no-referrer" data-modified="1" data-score="0.00"/>
          </div>
          <div>
            <div class="space-y-6">
              <div>
                <h3 class="font-semibold text-gray-900 mb-3 flex items-center gap-2">
                  <i class="fas fa-users text-orange-500"></i>
                  Target Community
                </h3>
                <p class="text-gray-700">
                  HouseFind Phoenix serves the underground electronic music community in Phoenix, Arizona,
                  connecting music lovers with intimate, authentic underground events.
                </p>
              </div>

              <div>
                <h3 class="font-semibold text-gray-900 mb-3 flex items-center gap-2">
                  <i class="fas fa-music text-purple-500"></i>
                  Platform Mission
                </h3>
                <p class="text-gray-700">
                  Our mission is to aggregate events from multiple sources to provide comprehensive coverage
                  of Phoenix&#39;s vibrant underground scene, helping music lovers discover their next favorite event.
                </p>
              </div>
            </div>
          </div>
        </div>

        <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-4">
          <div class="bg-gradient-to-br from-orange-50 to-orange-100 rounded-lg p-4 border border-orange-200">
            <i class="fas fa-sun text-orange-500 text-2xl mb-3"></i>
            <h4 class="font-semibold text-gray-900 mb-2">Desert-Inspired Techno</h4>
            <p class="text-gray-700 text-sm">Unique Phoenix sound influenced by desert landscapes and underground warehouse culture</p>
          </div>

          <div class="bg-gradient-to-br from-purple-50 to-purple-100 rounded-lg p-4 border border-purple-200">
            <i class="fas fa-home text-purple-500 text-2xl mb-3"></i>
            <h4 class="font-semibold text-gray-900 mb-2">Underground House</h4>
            <p class="text-gray-700 text-sm">Intimate gatherings in secret locations, showcasing local and touring talent</p>
          </div>

          <div class="bg-gradient-to-br from-blue-50 to-blue-100 rounded-lg p-4 border border-blue-200">
            <i class="fas fa-heart text-blue-500 text-2xl mb-3"></i>
            <h4 class="font-semibold text-gray-900 mb-2">Intimate Venues</h4>
            <p class="text-gray-700 text-sm">Small-capacity spaces that create authentic connections between artists and audience</p>
          </div>

          <div class="bg-gradient-to-br from-green-50 to-green-100 rounded-lg p-4 border border-green-200">
            <i class="fas fa-star text-green-500 text-2xl mb-3"></i>
            <h4 class="font-semibold text-gray-900 mb-2">Local Artist Showcases</h4>
            <p class="text-gray-700 text-sm">Platform dedicated to promoting Phoenix&#39;s talented local electronic music community</p>
          </div>
        </div>
      </section>

      <!-- Contributing -->
      <section id="contributing" class="mb-16">
        <h2 class="font-display text-3xl font-bold mb-8 text-gray-900">Contributing</h2>

        <div class="space-y-8">
          <div class="bg-gradient-to-r from-orange-50 to-teal-50 rounded-xl p-8 border border-orange-200">
            <h3 class="font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <i class="fas fa-heart text-red-500"></i>
              Built for the Community
            </h3>
            <p class="text-gray-700 mb-4">
              We welcome contributions to make HouseFind Phoenix even better for the community!
              Whether you&#39;re a developer, designer, or music enthusiast, there&#39;s a way to contribute.
            </p>
            <div class="flex flex-wrap gap-3">
              <span class="px-3 py-1 bg-orange-100 text-orange-800 rounded-full text-sm font-medium">Open Source</span>
              <span class="px-3 py-1 bg-teal-100 text-teal-800 rounded-full text-sm font-medium">Community Driven</span>
              <span class="px-3 py-1 bg-purple-100 text-purple-800 rounded-full text-sm font-medium">Music First</span>
            </div>
          </div>

          <div class="grid md:grid-cols-2 gap-8">
            <div>
              <h3 class="font-semibold text-gray-900 mb-4">Development Workflow</h3>
              <div class="space-y-4">
                <div class="flex items-start gap-3">
                  <div class="w-8 h-8 bg-gray-100 rounded-full flex items-center justify-center flex-shrink-0">
                    <span class="text-sm font-semibold text-gray-600">1</span>
                  </div>
                  <div>
                    <h4 class="font-medium text-gray-900">Fork the Repository</h4>
                    <p class="text-gray-600 text-sm">Create your own copy of the project to work on</p>
                  </div>
                </div>

                <div class="flex items-start gap-3">
                  <div class="w-8 h-8 bg-gray-100 rounded-full flex items-center justify-center flex-shrink-0">
                    <span class="text-sm font-semibold text-gray-600">2</span>
                  </div>
                  <div>
                    <h4 class="font-medium text-gray-900">Create a Feature Branch</h4>
                    <p class="text-gray-600 text-sm">Use descriptive branch names for your changes</p>
                  </div>
                </div>

                <div class="flex items-start gap-3">
                  <div class="w-8 h-8 bg-gray-100 rounded-full flex items-center justify-center flex-shrink-0">
                    <span class="text-sm font-semibold text-gray-600">3</span>
                  </div>
                  <div>
                    <h4 class="font-medium text-gray-900">Make Changes with Tests</h4>
                    <p class="text-gray-600 text-sm">Include tests for new features and bug fixes</p>
                  </div>
                </div>

                <div class="flex items-start gap-3">
                  <div class="w-8 h-8 bg-gray-100 rounded-full flex items-center justify-center flex-shrink-0">
                    <span class="text-sm font-semibold text-gray-600">4</span>
                  </div>
                  <div>
                    <h4 class="font-medium text-gray-900">Submit a Pull Request</h4>
                    <p class="text-gray-600 text-sm">Describe your changes and link to relevant issues</p>
                  </div>
                </div>
              </div>
            </div>

            <div>
              <h3 class="font-semibold text-gray-900 mb-4">Code Standards</h3>
              <div class="space-y-3">
                <div class="bg-white rounded-lg p-3 border border-gray-200">
                  <div class="flex items-center gap-2 mb-1">
                    <i class="fab fa-js-square text-yellow-500"></i>
                    <h4 class="font-medium text-gray-900">TypeScript Strict Mode</h4>
                  </div>
                  <p class="text-gray-600 text-sm">Full type safety with strict TypeScript configuration</p>
                </div>

                <div class="bg-white rounded-lg p-3 border border-gray-200">
                  <div class="flex items-center gap-2 mb-1">
                    <i class="fas fa-paint-brush text-blue-500"></i>
                    <h4 class="font-medium text-gray-900">ESLint + Prettier</h4>
                  </div>
                  <p class="text-gray-600 text-sm">Consistent code formatting and linting rules</p>
                </div>

                <div class="bg-white rounded-lg p-3 border border-gray-200">
                  <div class="flex items-center gap-2 mb-1">
                    <i class="fas fa-shield-alt text-green-500"></i>
                    <h4 class="font-medium text-gray-900">Error Handling</h4>
                  </div>
                  <p class="text-gray-600 text-sm">Comprehensive error handling with proper fallbacks</p>
                </div>

                <div class="bg-white rounded-lg p-3 border border-gray-200">
                  <div class="flex items-center gap-2 mb-1">
                    <i class="fas fa-rocket text-orange-500"></i>
                    <h4 class="font-medium text-gray-900">Performance First</h4>
                  </div>
                  <p class="text-gray-600 text-sm">Performance-conscious implementations with benchmarks</p>
                </div>
              </div>
            </div>
          </div>

          <div class="text-center bg-gray-100 rounded-xl p-8">
            <h3 class="font-semibold text-gray-900 mb-4">Ready to Contribute?</h3>
            <p class="text-gray-700 mb-6">
              Join our community of developers and music enthusiasts building the future of event discovery in Phoenix.
            </p>
            <div class="flex flex-col sm:flex-row gap-3 justify-center">
              <a href="#" class="inline-flex items-center px-4 py-2 bg-orange-500 text-white rounded-lg hover:bg-orange-600 transition-colors">
                <i class="fab fa-github mr-2"></i>
                View on GitHub
              </a>
              <a href="#" class="inline-flex items-center px-4 py-2 border border-gray-300 text-gray-700 rounded-lg hover:border-orange-500 hover:text-orange-500 transition-colors">
                <i class="fas fa-comments mr-2"></i>
                Join Discord
              </a>
            </div>
          </div>
        </div>
      </section>

      <!-- Footer -->
      <footer class="border-t border-gray-200 pt-8 pb-16">
        <div class="text-center space-y-4">
          <div class="flex justify-center items-center gap-2 text-gray-500">
            <i class="fas fa-music text-orange-500"></i>
            <span class="font-display text-lg font-medium">HouseFind Phoenix</span>
          </div>
          <p class="text-gray-600">
            Built with ❤️ for Phoenix&#39;s underground music community
          </p>
          <p class="text-gray-500 text-sm">
            Copyright © 2025 HouseFind Phoenix. All rights reserved.
          </p>
          <div class="flex justify-center gap-4 mt-6">
            <a href="#" class="text-gray-400 hover:text-orange-500 transition-colors">
              <i class="fab fa-github text-xl"></i>
            </a>
            <a href="#" class="text-gray-400 hover:text-orange-500 transition-colors">
              <i class="fab fa-discord text-xl"></i>
            </a>
            <a href="#" class="text-gray-400 hover:text-orange-500 transition-colors">
              <i class="fab fa-twitter text-xl"></i>
            </a>
          </div>
        </div>
      </footer>
    </div>
  

</body></html>
