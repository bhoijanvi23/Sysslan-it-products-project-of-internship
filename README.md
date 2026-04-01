# Sysslan-it-products-project-of-internship
A responsive e-commerce website clone built using HTML, CSS, featuring a modern UI and mobile-friendly design.

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sysslan IT | Premium Tech Hub</title>
    <style>
        /* --- GLOBAL STYLES --- */
        :root {
            --primary: #2c3e50;
            --accent: #3498db;
            --success: #27ae60;
            --bg: #f8f9fa;
            --white: #ffffff;
            --text: #333;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: var(--bg);
            color: var(--text);
            scroll-behavior: smooth;
        }

        /* --- HEADER & NAV --- */
        header {
            background: var(--primary);
            color: var(--white);
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 20px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 600;
        }

        nav ul li a:hover {
            color: var(--accent);
        }

        /* --- HERO SECTION (Adds Length) --- */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)),
                url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
            height: 60vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            text-align: center;
            padding: 0 20px;
        }

        .hero h2 {
            font-size: 3rem;
            margin-bottom: 10px;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 20px;
        }

        .btn-main {
            background: var(--accent);
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
            font-weight: bold;
        }

        /* --- PRODUCT GRID --- */
        main {
            max-width: 1200px;
            margin: 50px auto;
            padding: 0 20px;
        }

        .grid-header {
            text-align: center;
            margin-bottom: 40px;
        }

        .product-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
        }

        .product {
            background: var(--white);
            border-radius: 10px;
            padding: 15px;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
            transition: 0.3s;
            display: flex;
            flex-direction: column;
        }

        .product:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .tag {
            background: #eee;
            font-size: 0.7rem;
            padding: 3px 10px;
            border-radius: 15px;
            align-self: center;
            margin-bottom: 10px;
            font-weight: bold;
            color: #777;
        }

        .product img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            border-radius: 5px;
            margin-bottom: 15px;
        }

        .product h3 {
            font-size: 1.1rem;
            margin-bottom: 8px;
        }

        .product .desc {
            font-size: 0.85rem;
            color: #666;
            margin-bottom: 15px;
            flex-grow: 1;
        }

        .product .price {
            font-weight: bold;
            font-size: 1.2rem;
            margin-bottom: 15px;
            display: block;
        }

        .add-btn {
            background: var(--accent);
            color: white;
            border: none;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
        }

        /* --- CONTACT & FOOTER --- */
        #contact {
            background: white;
            padding: 60px 20px;
            text-align: center;
            margin-top: 50px;
        }

        #contact form {
            max-width: 600px;
            margin: 20px auto;
        }

        input,
        textarea {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        footer {
            background: var(--primary);
            color: white;
            padding: 40px 5%;
            text-align: center;
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                gap: 15px;
            }

            .hero h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>Sysslan IT</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Shop</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#" style="color: #3498db;">🛒 (<span id="cart-count">0</span>)</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero" id="home">
        <h2>Future Tech, Today.</h2>
        <p>Explore our wide range of premium electronics and accessories.</p>
        <a href="#products" class="btn-main">Start Shopping</a>
    </section>

    <main id="products">
        <div class="grid-header">
            <h2>Featured Products</h2>
            <p>Quality hand-picked items for your digital life.</p>
        </div>

        <div class="product-container">
            <article class="product">
                <span class="tag">Wearables</span>
                <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=400" alt="Watch">
                <h3>Smart Watch Elite</h3>
                <p class="desc">Heart rate monitoring and GPS tracking built-in.</p>
                <span class="price">$149.00</span>
                <button class="add-btn">Add to Cart</button>
            </article>

            <article class="product">
                <span class="tag">Audio</span>
                <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=400" alt="Audio">
                <h3>Pro Studio Headphones</h3>
                <p class="desc">High-fidelity sound with deep bass response.</p>
                <span class="price">$199.00</span>
                <button class="add-btn">Add to Cart</button>
            </article>

            <article class="product">
                <span class="tag">Gaming</span>
                <img src="https://images.unsplash.com/photo-1527690789675-4ea7d8da4fe3?w=400" alt="Gaming">
                <h3>Mechanical Keyboard</h3>
                <p class="desc">RGB backlit with customizable tactile switches.</p>
                <span class="price">$89.00</span>
                <button class="add-btn">Add to Cart</button>
            </article>

            <article class="product">
                <span class="tag">Accessories</span>
                <img src="https://images.unsplash.com/photo-1553062407-98eeb64c6a62?w=400" alt="Bag">
                <h3>Travel Tech Bag</h3>
                <p class="desc">Water-resistant with 15-inch laptop sleeve.</p>
                <span class="price">$55.00</span>
                <button class="add-btn">Add to Cart</button>
            </article>

            <article class="product">
                <span class="tag">Computing</span>
                <img src="https://images.unsplash.com/photo-1527864550417-7fd91fc51a46?w=400" alt="Mouse">
                <h3>Ergonomic Mouse</h3>
                <p class="desc">Wireless precision for all-day productivity.</p>
                <span class="price">$45.00</span>
                <button class="add-btn">Add to Cart</button>
            </article>

            <article class="product">
                <span class="tag">Audio</span>
                <img src="https://images.unsplash.com/photo-1590658268037-6bf12165a8df?w=400" alt="Buds">
                <h3>PureSound Earbuds</h3>
                <p class="desc">Ultra-lightweight with noise-canceling tech.</p>
                <span class="price">$120.00</span>
                <button class="add-btn">Add to Cart</button>
            </article>

            <article class="product">
                <span class="tag">Office</span>
                <img src="https://images.unsplash.com/photo-1515343483479-4453509b14fd?w=400" alt="Monitor">
                <h3>4K Curved Monitor</h3>
                <p class="desc">Immersive 32-inch display for gaming and work.</p>
                <span class="price">$350.00</span>
                <button class="add-btn">Add to Cart</button>
            </article>

            <article class="product">
                <span class="tag">Wearables</span>
                <img src="https://images.unsplash.com/photo-1575311373937-040b8e1fd5b6?w=400" alt="Fitness">
                <h3>Fitness Tracker Z</h3>
                <p class="desc">7-day battery life with sleep tracking.</p>
                <span class="price">$39.00</span>
                <button class="add-btn">Add to Cart</button>
            </article>
        </div>
    </main>

    <section id="contact">
        <h2>Get In Touch</h2>
        <form id="contactForm">
            <input type="text" id="name" placeholder="Name" required>
            <input type="email" id="email" placeholder="Email" required>
            <textarea rows="5" placeholder="Message" required></textarea>
            <button type="submit" class="btn-main">Send Message</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2026 Sysslan IT Products. Premium Quality. Worldwide Shipping.</p>
    </footer>

    <script>
        let count = 0;
        const cartDisplay = document.getElementById('cart-count');
        const buttons = document.querySelectorAll('.add-btn');

        buttons.forEach(btn => {
            btn.addEventListener('click', () => {
                count++;
                cartDisplay.innerText = count;
                btn.innerText = "Added ✓";
                btn.style.background = "#27ae60";
                setTimeout(() => {
                    btn.innerText = "Add to Cart";
                    btn.style.background = "#3498db";
                }, 800);
            });
        });

        document.getElementById('contactForm').addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Success! We will contact you soon.');
            e.target.reset();
        });
    </script>
</body>

</html>
