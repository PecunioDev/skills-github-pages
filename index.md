<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pecunio | Tax & Accounting Services</title>
    <style>
        :root {
            --primary: #2e7d32;
            --primary-light: #4caf50;
            --primary-dark: #1b5e20;
            --secondary: #f5f5f5;
            --text: #333333;
            --text-light: #666666;
            --white: #ffffff;
            --gray-light: #f9f9f9;
            --gray: #e0e0e0;
            --gray-dark: #9e9e9e;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            color: var(--text);
            line-height: 1.6;
        }

        h1, h2, h3, h4 {
            margin-bottom: 1rem;
            font-weight: 600;
        }

        p {
            margin-bottom: 1rem;
            color: var(--text-light);
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            background: var(--primary);
            color: var(--white);
            text-decoration: none;
            border-radius: 4px;
            font-weight: 500;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        .btn-outline:hover {
            background: var(--primary);
            color: var(--white);
        }

        /* Header */
        header {
            padding: 1.5rem 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            background: var(--white);
            z-index: 1000;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text);
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .mobile-menu {
            display: none;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            padding: 10rem 0 6rem;
            background: linear-gradient(135deg, var(--gray-light) 0%, var(--white) 100%);
        }

        .hero-content {
            display: flex;
            align-items: center;
            gap: 4rem;
        }

        .hero-text {
            flex: 1;
        }

        .hero-text h1 {
            font-size: 3.2rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }

        .hero-text h1 span {
            color: var(--primary);
        }

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
        }

        .hero-image img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }

        .hero-cta {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
        }

        /* Features Section */
        .features {
            padding: 6rem 0;
            background: var(--white);
        }

        .section-heading {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-heading h2 {
            font-size: 2.5rem;
            color: var(--text);
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 3rem;
        }

        .feature-card {
            padding: 2rem;
            background: var(--gray-light);
            border-radius: 8px;
            transition: all 0.3s ease;
            border: 1px solid var(--gray);
            height: 100%;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
            border-color: var(--primary-light);
        }

        .feature-icon {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        /* Pricing Section */
        .pricing {
            padding: 6rem 0;
            background: var(--gray-light);
        }

        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
        }

        .pricing-card {
            background: var(--white);
            border-radius: 8px;
            padding: 2.5rem;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid var(--gray);
            height: 100%;
            display: flex;
            flex-direction: column;
        }

        .pricing-card:hover {
            transform: scale(1.03);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .popular {
            border-color: var(--primary);
            position: relative;
        }

        .popular::before {
            content: "Most Popular";
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--primary);
            color: var(--white);
            padding: 0.5rem 1.5rem;
            border-radius: 30px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .price {
            font-size: 3rem;
            font-weight: 700;
            margin: 1.5rem 0;
            color: var(--primary);
        }

        .price span {
            font-size: 1rem;
            color: var(--text-light);
        }

        .pricing-features {
            list-style: none;
            margin: 2rem 0;
            flex-grow: 1;
        }

        .pricing-features li {
            margin-bottom: 1rem;
            color: var(--text-light);
        }

        .pricing-features li.included {
            color: var(--text);
            font-weight: 500;
        }

        .pricing-features li.included::before {
            content: "✓";
            color: var(--primary);
            margin-right: 0.5rem;
            font-weight: bold;
        }

        /* Testimonials Section */
        .testimonials {
            padding: 6rem 0;
            background: var(--white);
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 3rem;
        }

        .testimonial-card {
            padding: 2rem;
            background: var(--gray-light);
            border-radius: 8px;
            border: 1px solid var(--gray);
        }

        .testimonial-content {
            font-style: italic;
            margin-bottom: 1.5rem;
        }

        .client-info {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .client-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-weight: bold;
        }

        .client-details h4 {
            margin-bottom: 0.2rem;
        }

        .client-details p {
            margin-bottom: 0;
            font-size: 0.9rem;
        }

        /* Contact Section */
        .contact {
            padding: 6rem 0;
            background: var(--gray-light);
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: var(--white);
            padding: 3rem;
            border-radius: 8px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-control {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid var(--gray);
            border-radius: 4px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(46, 125, 50, 0.2);
        }

        textarea.form-control {
            resize: vertical;
            min-height: 120px;
        }

        /* Footer */
        footer {
            background: var(--primary-dark);
            color: var(--white);
            padding: 4rem 0 2rem;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .footer-links h3 {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 0.8rem;
        }

        .footer-links a {
            color: var(--gray-light);
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .footer-links a:hover {
            color: var(--white);
            text-decoration: underline;
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gray-light);
            font-size: 0.9rem;
        }

        /* Mobile styles */
        @media (max-width: 992px) {
            .feature-grid, .pricing-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .footer-grid {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 768px) {
            .hero-content {
                flex-direction: column;
                gap: 3rem;
                text-align: center;
            }
            
            .hero-cta {
                justify-content: center;
            }
            
            .hero-text h1 {
                font-size: 2.5rem;
            }
            
            .feature-grid, .pricing-grid, .testimonial-grid, .footer-grid {
                grid-template-columns: 1fr;
            }
            
            .nav-links {
                display: none;
            }
            
            .mobile-menu {
                display: block;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Pecunio</div>
                <div class="nav-links">
                    <a href="#services">Services</a>
                    <a href="#pricing">Pricing</a>
                    <a href="#testimonials">Testimonials</a>
                    <a href="#contact">Contact</a>
                </div>
                <div class="mobile-menu">☰</div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Smart <span>Tax & Accounting</span> Solutions for Your Business</h1>
                    <p>Pecunio helps businesses of all sizes streamline their finances, minimize tax burdens, and make confident financial decisions with our expert accounting services.</p>
                    <div class="hero-cta">
                        <a href="#contact" class="btn">Get Started</a>
                        <a href="#services" class="btn btn-outline">Explore Services</a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="/api/placeholder/500/400" alt="Pecunio Tax & Accounting Services">
                </div>
            </div>
        </div>
    </section>

    <!-- Features/Services Section -->
    <section class="features" id="services">
        <div class="container">
            <div class="section-heading">
                <h2>Our Services</h2>
                <p>Comprehensive financial solutions designed to help your business thrive</p>
            </div>
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon">📊</div>
                    <h3>Tax Planning & Preparation</h3>
                    <p>Strategic tax planning to minimize your tax burden and ensure compliance with all regulations. We handle personal and business tax returns with meticulous attention to detail.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📒</div>
                    <h3>Bookkeeping & Financial Statements</h3>
                    <p>Accurate and timely bookkeeping services to keep your financials organized. Regular financial statements to give you clear insights into your business performance.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📈</div>
                    <h3>Business Advisory</h3>
                    <p>Expert guidance on financial strategy, business growth, cash flow management, and budgeting to help your business reach its full potential.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🏢</div>
                    <h3>Corporate Accounting</h3>
                    <p>Complete corporate accounting solutions including entity formation, compliance, payroll services, and corporate tax strategies tailored to your business needs.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">💼</div>
                    <h3>Audit Support & Representation</h3>
                    <p>Professional representation during tax audits and proactive assistance to help you navigate the complex audit process with confidence.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">💰</div>
                    <h3>Wealth Management</h3>
                    <p>Holistic financial planning services to help you build and preserve wealth, plan for retirement, and achieve your long-term financial goals.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section class="pricing" id="pricing">
        <div class="container">
            <div class="section-heading">
                <h2>Transparent Pricing</h2>
                <p>Flexible plans designed to fit businesses of all sizes</p>
            </div>
            <div class="pricing-grid">
                <div class="pricing-card">
                    <h3>Startup</h3>
                    <div class="price">$299<span>/month</span></div>
                    <p>Perfect for new businesses just getting started with their finances</p>
                    <ul class="pricing-features">
                        <li class="included">Monthly Bookkeeping</li>
                        <li class="included">Basic Financial Statements</li>
                        <li class="included">Annual Tax Preparation</li>
                        <li class="included">Quarterly Tax Planning</li>
                        <li>Business Advisory</li>
                        <li>Payroll Services</li>
                    </ul>
                    <a href="#contact" class="btn btn-outline">Get Started</a>
                </div>
                <div class="pricing-card popular">
                    <h3>Growth</h3>
                    <div class="price">$599<span>/month</span></div>
                    <p>Ideal for growing businesses with increasing financial complexity</p>
                    <ul class="pricing-features">
                        <li class="included">Monthly Bookkeeping</li>
                        <li class="included">Comprehensive Financial Statements</li>
                        <li class="included">Annual Tax Preparation</li>
                        <li class="included">Monthly Tax Planning</li>
                        <li class="included">Business Advisory (2 hours/month)</li>
                        <li class="included">Payroll Services (up to 10 employees)</li>
                    </ul>
                    <a href="#contact" class="btn">Get Started</a>
                </div>
                <div class="pricing-card">
                    <h3>Enterprise</h3>
                    <div class="price">$999<span>/month</span></div>
                    <p>Comprehensive solution for established businesses with complex needs</p>
                    <ul class="pricing-features">
                        <li class="included">Weekly Bookkeeping Updates</li>
                        <li class="included">Advanced Financial Statements & Analysis</li>
                        <li class="included">Annual Tax Preparation</li>
                        <li class="included">Continuous Tax Planning</li>
                        <li class="included">Unlimited Business Advisory</li>
                        <li class="included">Complete Payroll Services</li>
                    </ul>
                    <a href="#contact" class="btn btn-outline">Get Started</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="section-heading">
                <h2>Client Success Stories</h2>
                <p>Hear from businesses that have transformed their finances with Pecunio</p>
            </div>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        "Switching to Pecunio was one of the best business decisions we've made. They helped us restructure our finances, saving us over $45,000 in taxes last year alone. Their strategic approach to financial planning has been instrumental in our growth."
                    </div>
                    <div class="client-info">
                        <div class="client-avatar">JM</div>
                        <div class="client-details">
                            <h4>Jennifer Malone</h4>
                            <p>CEO, TechNova Solutions</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        "As a small business owner, I was overwhelmed by the financial aspects of my company. Pecunio simplified everything and provided clear guidance. Their team is responsive, knowledgeable, and genuinely cares about our success."
                    </div>
                    <div class="client-info">
                        <div class="client-avatar">RK</div>
                        <div class="client-details">
                            <h4>Robert Kim</h4>
                            <p>Owner, Riverfront Cafe</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        "We've been with Pecunio for over five years, and they consistently exceed our expectations. Their proactive tax planning and business advisory services have helped us navigate complex financial challenges with confidence."
                    </div>
                    <div class="client-info">
                        <div class="client-avatar">SJ</div>
                        <div class="client-details">
                            <h4>Sarah Johnson</h4>
                            <p>CFO, Meridian Manufacturing</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        "Pecunio's team took the time to understand our unique business model and created a customized financial strategy. Their expertise has been invaluable in helping us scale while maintaining profitability."
                    </div>
                    <div class="client-info">
                        <div class="client-avatar">DH</div>
                        <div class="client-details">
                            <h4>David Hernandez</h4>
                            <p>Founder, Elevate Marketing Group</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-heading">
                <h2>Get Started Today</h2>
                <p>Schedule a free consultation to discuss your business needs</p>
            </div>
            <div class="contact-form">
                <form id="leadForm">
                    <div class="form-group">
                        <label for="name" class="form-label">Full Name</label>
                        <input type="text" id="name" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="email" class="form-label">Email Address</label>
                        <input type="email" id="email" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <label for="phone" class="form-label">Phone Number</label>
                        <input type="tel" id="phone" class="form-control">
                    </div>
                    <div class="form-group">
                        <label for="company" class="form-label">Company Name</label>
                        <input type="text" id="company" class="form-control">
                    </div>
                    <div class="form-group">
                        <label for="service" class="form-label">Service of Interest</label>
                        <select id="service" class="form-control">
                            <option value="tax">Tax Planning & Preparation</option>
                            <option value="bookkeeping">Bookkeeping & Financial Statements</option>
                            <option value="advisory">Business Advisory</option>
                            <option value="corporate">Corporate Accounting</option>
                            <option value="audit">Audit Support</option>
                            <option value="wealth">Wealth Management</option>
                            <option value="other">Other</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="message" class="form-label">Tell us about your needs</label>
                        <textarea id="message" class="form-control"></textarea>
                    </div>
                    <button type="submit" class="btn" style="width: 100%;">Request Free Consultation</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-about">
                    <div class="footer-logo">Pecunio</div>
                    <p>Professional tax and accounting services to help your business thrive financially. We combine expertise with personalized attention to deliver exceptional results.</p>
                </div>
                <div class="footer-links">
                    <h3>Services</h3>
                    <ul>
                        <li><a href="#services">Tax Planning</a></li>
                        <li><a href="#services">Bookkeeping</a></li>
                        <li><a href="#services">Business Advisory</a></li>
                        <li><a href="#services">Corporate Accounting</a></li>
                        <li><a href="#services">Audit Support</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h3>Company</h3>
                    <ul>
                        <li><a href="#">About Us</a></li>
                        <li><a href="#">Our Team</a></li>
                        <li><a href="#">Careers</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h3>Contact</h3>
                    <ul>
                        <li>123 Finance Street</li>
                        <li>Suite 500</li>
                        <li>New York, NY 10001</li>
                        <li>info@pecunio.com</li>
                        <li>(555) 123-4567</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2025 Pecunio. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Simple form submission handler
        document.getElementById('leadForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const phone = document.getElementById('phone').value;
            const company = document.getElementById('company').value;
            const service = document.getElementById('service').value;
            const message = document.getElementById('message').value;
            
            // In a real implementation, you would send this data to your server
            console.log('Form submitted:', { name, email, phone, company, service, message });
            
            // Show success message
            alert('Thank you for your interest! Our team will contact you within 24 hours to schedule your free consultation.');
            
            // Reset form
            this.reset();
        });
        
        // Mobile menu toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            const navLinks = document.querySelector('.nav-links');
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
