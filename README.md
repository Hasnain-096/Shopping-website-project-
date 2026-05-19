# Shopping-website-project-
An online shopping website created for people to explore designer designed articles from home providing a global access 

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>UrbanCart | Modern Shopping Layout</title>
  <!-- Google Fonts & simple CSS reset -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 (free icons) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background-color: #fafafc;
      color: #1e1e2a;
      line-height: 1.4;
    }

    /* container utility */
    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 24px;
    }

    /* ========== HEADER / NAVIGATION ========== */
    .site-header {
      background: white;
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.03), 0 4px 8px rgba(0, 0, 0, 0.02);
      position: sticky;
      top: 0;
      z-index: 100;
      backdrop-filter: blur(0px);
      border-bottom: 1px solid #eef2f6;
    }

    .header-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 16px;
      padding: 16px 0;
    }

    .logo-area {
      display: flex;
      align-items: baseline;
      gap: 6px;
    }
    .logo-icon {
      font-size: 28px;
      color: #2b6e4f;
    }
    .logo-text {
      font-weight: 700;
      font-size: 1.7rem;
      letter-spacing: -0.3px;
      background: linear-gradient(135deg, #1f5e44, #2b7a5c);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
    }
    .logo-badge {
      font-size: 0.7rem;
      background: #eef2f6;
      padding: 2px 8px;
      border-radius: 30px;
      font-weight: 500;
      color: #2b6e4f;
    }

    /* search bar */
    .search-wrapper {
      flex: 1;
      max-width: 400px;
      min-width: 200px;
    }
    .search-box {
      display: flex;
      background: #f3f4f6;
      border-radius: 60px;
      padding: 6px 6px 6px 18px;
      align-items: center;
      border: 1px solid #e4e7eb;
      transition: all 0.2s;
    }
    .search-box:focus-within {
      background: white;
      border-color: #2b6e4f;
      box-shadow: 0 0 0 3px rgba(43, 110, 79, 0.1);
    }
    .search-box i {
      color: #8f9aa8;
      font-size: 1rem;
    }
    .search-box input {
      flex: 1;
      border: none;
      background: transparent;
      padding: 10px 8px;
      font-size: 0.95rem;
      outline: none;
      font-weight: 400;
    }
    .search-box button {
      background: #2b6e4f;
      border: none;
      color: white;
      padding: 8px 20px;
      border-radius: 40px;
      font-weight: 500;
      cursor: pointer;
      transition: 0.2s;
      font-size: 0.85rem;
    }
    .search-box button:hover {
      background: #1f5e44;
    }

    /* right icons */
    .nav-icons {
      display: flex;
      gap: 22px;
      align-items: center;
    }
    .icon-link {
      display: flex;
      flex-direction: column;
      align-items: center;
      font-size: 0.75rem;
      color: #2c3e42;
      transition: color 0.2s;
      cursor: pointer;
      text-decoration: none;
      gap: 4px;
    }
    .icon-link i {
      font-size: 1.35rem;
    }
    .icon-link:hover {
      color: #2b6e4f;
    }
    .cart-badge {
      position: relative;
    }
    .cart-count {
      position: absolute;
      top: -8px;
      right: -12px;
      background: #e85d4f;
      color: white;
      font-size: 0.65rem;
      font-weight: bold;
      border-radius: 30px;
      padding: 2px 6px;
      min-width: 18px;
      text-align: center;
    }

    /* category bar */
    .category-bar {
      background: white;
      border-bottom: 1px solid #eef2f6;
      padding: 12px 0;
      overflow-x: auto;
      white-space: nowrap;
      scrollbar-width: thin;
    }
    .category-list {
      display: flex;
      gap: 28px;
      align-items: center;
    }
    .category-item {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      font-weight: 500;
      color: #4a5b66;
      font-size: 0.9rem;
      cursor: pointer;
      transition: 0.2s;
      padding: 4px 0;
      border-bottom: 2px solid transparent;
    }
    .category-item i {
      font-size: 1rem;
    }
    .category-item:hover, .category-item.active {
      color: #2b6e4f;
      border-bottom-color: #2b6e4f;
    }

    /* hero / banner section */
    .hero {
      margin: 32px 0 40px 0;
    }
    .hero-card {
      background: linear-gradient(110deg, #eef6f2 0%, #e2f0ea 100%);
      border-radius: 32px;
      padding: 40px 40px;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
    }
    .hero-text h1 {
      font-size: 2.4rem;
      font-weight: 700;
      letter-spacing: -0.02em;
      line-height: 1.2;
      color: #1f3830;
    }
    .hero-text p {
      margin-top: 16px;
      color: #3e5a50;
      max-width: 420px;
    }
    .hero-btn {
      margin-top: 24px;
      background: #1e3a2f;
      border: none;
      padding: 12px 32px;
      border-radius: 40px;
      color: white;
      font-weight: 600;
      cursor: pointer;
      transition: 0.2s;
      font-size: 0.9rem;
    }
    .hero-btn:hover {
      background: #2b6e4f;
    }
    .hero-badge {
      background: rgba(255,255,240,0.8);
      padding: 6px 18px;
      border-radius: 40px;
      font-size: 0.8rem;
      font-weight: 500;
      display: inline-block;
      margin-bottom: 12px;
    }

    /* product grid */
    .section-title {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      flex-wrap: wrap;
      margin: 40px 0 20px 0;
    }
    .section-title h2 {
      font-size: 1.8rem;
      font-weight: 600;
      letter-spacing: -0.3px;
    }
    .view-all {
      color: #2b6e4f;
      font-weight: 500;
      cursor: pointer;
      font-size: 0.9rem;
    }

    .products-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 28px;
      margin-bottom: 60px;
    }

    .product-card {
      background: white;
      border-radius: 24px;
      overflow: hidden;
      transition: transform 0.25s ease, box-shadow 0.25s;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.02), 0 1px 2px rgba(0,0,0,0.03);
      border: 1px solid #edf2f7;
    }
    .product-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 20px 25px -12px rgba(0, 0, 0, 0.08);
      border-color: #dce5ec;
    }
    .product-img {
      background-color: #f5f7fa;
      height: 220px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 4rem;
      color: #6c8d7c;
    }
    .product-info {
      padding: 18px 16px 20px;
    }
    .product-title {
      font-weight: 600;
      font-size: 1.1rem;
      margin-bottom: 6px;
    }
    .product-category {
      font-size: 0.75rem;
      color: #7e8c8d;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin-bottom: 12px;
    }
    .price-row {
      display: flex;
      align-items: center;
      gap: 12px;
      margin: 12px 0;
    }
    .current-price {
      font-weight: 700;
      font-size: 1.4rem;
      color: #1f3830;
    }
    .old-price {
      text-decoration: line-through;
      font-size: 0.85rem;
      color: #9aaeb4;
    }
    .add-to-cart {
      width: 100%;
      background: #f0f4f9;
      border: none;
      padding: 12px 0;
      border-radius: 40px;
      font-weight: 600;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      color: #2b6e4f;
      cursor: pointer;
      transition: all 0.2s;
      margin-top: 12px;
    }
    .add-to-cart:hover {
      background: #2b6e4f;
      color: white;
    }

    /* footer */
    .site-footer {
      background: #ffffff;
      border-top: 1px solid #eef2f6;
      margin-top: 40px;
      padding: 48px 0 32px;
    }
    .footer-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 40px;
      margin-bottom: 32px;
    }
    .footer-col h4 {
      font-size: 1rem;
      margin-bottom: 18px;
      font-weight: 600;
    }
    .footer-col p, .footer-col a {
      color: #5a6e7a;
      font-size: 0.85rem;
      text-decoration: none;
      display: block;
      margin-bottom: 12px;
    }
    .copyright {
      text-align: center;
      padding-top: 24px;
      border-top: 1px solid #edf2f7;
      font-size: 0.8rem;
      color: #7e8c8d;
    }

    /* simple cart toast simulation */
    .toast-msg {
      position: fixed;
      bottom: 24px;
      right: 24px;
      background: #1e3a2f;
      color: white;
      padding: 12px 24px;
      border-radius: 60px;
      font-size: 0.9rem;
      font-weight: 500;
      z-index: 200;
      box-shadow: 0 8px 20px rgba(0,0,0,0.1);
      transition: opacity 0.2s;
      pointer-events: none;
    }

    /* ========== CART SIDEBAR (MAKES CART ACCESSIBLE) ========== */
    .cart-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5);
      z-index: 1000;
      visibility: hidden;
      opacity: 0;
      transition: visibility 0.3s, opacity 0.3s;
    }
    .cart-overlay.open {
      visibility: visible;
      opacity: 1;
    }
    .cart-sidebar {
      position: fixed;
      top: 0;
      right: 0;
      width: 100%;
      max-width: 480px;
      height: 100%;
      background: white;
      box-shadow: -5px 0 30px rgba(0, 0, 0, 0.1);
      z-index: 1001;
      transform: translateX(100%);
      transition: transform 0.3s ease;
      display: flex;
      flex-direction: column;
      font-family: 'Inter', sans-serif;
    }
    .cart-overlay.open .cart-sidebar {
      transform: translateX(0);
    }
    .cart-header {
      padding: 24px;
      border-bottom: 1px solid #eef2f6;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .cart-header h3 {
      font-size: 1.5rem;
      font-weight: 600;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .close-cart {
      background: none;
      border: none;
      font-size: 1.8rem;
      cursor: pointer;
      color: #8f9aa8;
      transition: color 0.2s;
    }
    .close-cart:hover {
      color: #e85d4f;
    }
    .cart-items-container {
      flex: 1;
      overflow-y: auto;
      padding: 16px 20px;
    }
    .cart-item {
      display: flex;
      gap: 16px;
      padding: 16px 0;
      border-bottom: 1px solid #f0f2f5;
      align-items: center;
    }
    .cart-item-icon {
      width: 60px;
      height: 60px;
      background: #f5f7fa;
      border-radius: 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.8rem;
      color: #2b6e4f;
    }
    .cart-item-details {
      flex: 1;
    }
    .cart-item-name {
      font-weight: 600;
      margin-bottom: 6px;
    }
    .cart-item-price {
      font-size: 0.85rem;
      color: #2b6e4f;
      font-weight: 500;
    }
    .cart-item-actions {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-top: 8px;
    }
    .qty-btn {
      background: #f0f4f9;
      border: none;
      width: 28px;
      height: 28px;
      border-radius: 30px;
      cursor: pointer;
      font-weight: bold;
      transition: 0.2s;
    }
    .qty-btn:hover {
      background: #2b6e4f;
      color: white;
    }
    .item-quantity {
      font-weight: 600;
      min-width: 24px;
      text-align: center;
    }
    .remove-item {
      background: none;
      border: none;
      color: #e85d4f;
      cursor: pointer;
      font-size: 0.8rem;
      margin-left: 8px;
      padding: 4px 8px;
      border-radius: 20px;
    }
    .remove-item:hover {
      background: #fee2e0;
    }
    .cart-footer {
      padding: 20px 24px 30px;
      border-top: 1px solid #eef2f6;
      background: white;
    }
    .cart-total {
      display: flex;
      justify-content: space-between;
      font-size: 1.2rem;
      font-weight: 700;
      margin-bottom: 20px;
    }
    .checkout-btn {
      width: 100%;
      background: #2b6e4f;
      color: white;
      border: none;
      padding: 14px;
      border-radius: 60px;
      font-weight: 600;
      font-size: 1rem;
      cursor: pointer;
      transition: 0.2s;
    }
    .checkout-btn:hover {
      background: #1f5e44;
    }
    .empty-cart-msg {
      text-align: center;
      padding: 48px 20px;
      color: #8f9aa8;
    }
    @media (max-width: 560px) {
      .cart-sidebar {
        max-width: 100%;
      }
    }
  </style>
</head>
<body>

<header class="site-header">
  <div class="container">
    <div class="header-inner">
      <div class="logo-area">
        <i class="fas fa-store logo-icon"></i>
        <span class="logo-text">UrbanCart</span>
        <span class="logo-badge">fresh</span>
      </div>
      <div class="search-wrapper">
        <div class="search-box">
          <i class="fas fa-search"></i>
          <input type="text" placeholder="Search for sneakers, jackets, electronics..." id="searchInput">
          <button id="searchBtn"><i class="fas fa-arrow-right"></i> Find</button>
        </div>
      </div>
      <div class="nav-icons">
        <div class="icon-link">
          <i class="far fa-user"></i>
          <span>Account</span>
        </div>
        <div class="icon-link cart-badge" id="cartIcon">
          <i class="fas fa-shopping-bag"></i>
          <span class="cart-count" id="cartCount">0</span>
          <span>Cart</span>
        </div>
      </div>
    </div>
  </div>
  <div class="category-bar">
    <div class="container">
      <div class="category-list">
        <div class="category-item active" data-cat="all"><i class="fas fa-fire"></i> All</div>
        <div class="category-item" data-cat="mens"><i class="fas fa-tshirt"></i> Men's</div>
        <div class="category-item" data-cat="womens"><i class="fas fa-female"></i> Women's</div>
        <div class="category-item" data-cat="electronics"><i class="fas fa-laptop-code"></i> Electronics</div>
        <div class="category-item" data-cat="accessories"><i class="fas fa-gem"></i> Accessories</div>
      </div>
    </div>
  </div>
</header>

<main class="container">
  <div class="hero">
    <div class="hero-card">
      <div class="hero-text">
        <div class="hero-badge"><i class="fas fa-gift"></i> summer sale</div>
        <h1>Up to 40% off<br>streetwear essentials</h1>
        <p>Fresh styles, free shipping & easy returns. Shop the new collection.</p>
        <button class="hero-btn">Shop Now →</button>
      </div>
      <div style="font-size: 5rem; opacity: 0.7;"><i class="fas fa-shopping-bag"></i> 🛍️</div>
    </div>
  </div>

  <div class="section-title">
    <h2>🔥 Featured for you</h2>
    <div class="view-all">View all →</div>
  </div>

  <div class="products-grid" id="productsGrid">
    <!-- products injected -->
  </div>
</main>

<footer class="site-footer">
  <div class="container">
    <div class="footer-grid">
      <div class="footer-col">
        <h4>UrbanCart</h4>
        <p>Sustainable fashion & tech<br>Delivering joy worldwide.</p>
      </div>
      <div class="footer-col">
        <h4>Shop</h4>
        <a href="#">Men</a>
        <a href="#">Women</a>
        <a href="#">Electronics</a>
        <a href="#">Accessories</a>
      </div>
      <div class="footer-col">
        <h4>Support</h4>
        <a href="#">Help Center</a>
        <a href="#">Returns</a>
        <a href="#">Track Order</a>
      </div>
      <div class="footer-col">
        <h4>Follow</h4>
        <a href="#"><i class="fab fa-instagram"></i> Instagram</a>
        <a href="#"><i class="fab fa-twitter"></i> Twitter</a>
      </div>
    </div>
    <div class="copyright">
      © 2026 UrbanCart — clean layout for modern shopping
    </div>
  </div>
</footer>

<div id="toast" class="toast-msg" style="opacity:0; visibility:hidden;">Added to cart</div>

<!-- CART SIDEBAR - MAKES CART ACCESSIBLE -->
<div id="cartOverlay" class="cart-overlay">
  <div class="cart-sidebar">
    <div class="cart-header">
      <h3><i class="fas fa-shopping-bag"></i> Your Cart</h3>
      <button class="close-cart" id="closeCartBtn">&times;</button>
    </div>
    <div class="cart-items-container" id="cartItemsContainer">
      <div class="empty-cart-msg">Your cart is empty. Start shopping!</div>
    </div>
    <div class="cart-footer" id="cartFooter" style="display: none;">
      <div class="cart-total">
        <span>Total</span>
        <span id="cartTotalPrice">$0.00</span>
      </div>
      <button class="checkout-btn" id="checkoutBtn">Proceed to Checkout →</button>
    </div>
  </div>
</div>

<script>
  // ---------- PRODUCT DATA ----------
  const products = [
    { id: 1, name: "Quilted Bomber Jacket", category: "mens", price: 89.99, oldPrice: 129.99, icon: "fa-vest" },
    { id: 2, name: "Slim Fit Chino Pants", category: "mens", price: 59.99, oldPrice: 79.99, icon: "fa-tshirt" },
    { id: 3, name: "Oversized Knit Sweater", category: "womens", price: 69.99, oldPrice: 99.99, icon: "fa-tshirt" },
    { id: 4, name: "High-Waist Trousers", category: "womens", price: 74.99, oldPrice: 99.99, icon: "fa-female" },
    { id: 5, name: "Wireless Noise Cancelling", category: "electronics", price: 199.99, oldPrice: 279.99, icon: "fa-headphones" },
    { id: 6, name: "Smartwatch Ultra", category: "electronics", price: 149.99, oldPrice: 229.99, icon: "fa-clock" },
    { id: 7, name: "Minimalist Backpack", category: "accessories", price: 49.99, oldPrice: 69.99, icon: "fa-bag-shopping" },
    { id: 8, name: "Retro Sunglasses", category: "accessories", price: 29.99, oldPrice: 59.99, icon: "fa-glasses" },
    { id: 9, name: "Leather Sneakers", category: "mens", price: 109.99, oldPrice: 159.99, icon: "fa-shoe-prints" },
    { id: 10, name: "Silk Midi Dress", category: "womens", price: 84.99, oldPrice: 119.99, icon: "fa-dress" }
  ];

  // ---------- CART STATE ----------
  let cart = [];  // each item: { id, name, price, quantity, icon }

  // Helper functions
  function findCartItem(productId) {
    return cart.find(item => item.id === productId);
  }

  function saveCartToLocal() {
    localStorage.setItem('urbanCart', JSON.stringify(cart));
  }

  function loadCartFromLocal() {
    const saved = localStorage.getItem('urbanCart');
    if (saved) {
      try {
        cart = JSON.parse(saved);
      } catch(e) { cart = []; }
    } else {
      cart = [];
    }
    updateAllCartUI();
  }

  function addToCart(productId) {
    const product = products.find(p => p.id === productId);
    if (!product) return;
    
    const existing = findCartItem(productId);
    if (existing) {
      existing.quantity += 1;
      showToast(`🛒 ${product.name} quantity: ${existing.quantity}`);
    } else {
      cart.push({
        id: product.id,
        name: product.name,
        price: product.price,
        quantity: 1,
        icon: product.icon
      });
      showToast(`✨ ${product.name} added to cart`);
    }
    saveCartToLocal();
    updateAllCartUI();
  }

  function updateQuantity(productId, delta) {
    const item = findCartItem(productId);
    if (!item) return;
    const newQty = item.quantity + delta;
    if (newQty <= 0) {
      removeItemCompletely(productId);
    } else {
      item.quantity = newQty;
      saveCartToLocal();
      updateAllCartUI();
      showToast(`🛍️ ${item.name} quantity: ${item.quantity}`);
    }
  }

  function removeItemCompletely(productId) {
    const item = findCartItem(productId);
    if (item) {
      cart = cart.filter(i => i.id !== productId);
      saveCartToLocal();
      updateAllCartUI();
      showToast(`🗑️ ${item.name} removed from cart`);
    }
  }

  function getCartTotal() {
    return cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
  }

  function getTotalItems() {
    return cart.reduce((sum, item) => sum + item.quantity, 0);
  }

  // Update header badge + cart sidebar + footer visibility
  function updateAllCartUI() {
    // header counter
    const cartCountSpan = document.getElementById('cartCount');
    if (cartCountSpan) cartCountSpan.textContent = getTotalItems();
    
    // render cart sidebar
    const container = document.getElementById('cartItemsContainer');
    const footer = document.getElementById('cartFooter');
    if (!container) return;
    
    if (cart.length === 0) {
      container.innerHTML = `<div class="empty-cart-msg"><i class="fas fa-bag-shopping" style="font-size: 3rem; opacity: 0.5; margin-bottom: 12px; display: block;"></i>Your cart is empty.<br>Add some cool items!</div>`;
      if (footer) footer.style.display = 'none';
      return;
    }
    
    if (footer) footer.style.display = 'block';
    container.innerHTML = cart.map(item => {
      const iconClass = item.icon || 'fa-bag-shopping';
      return `
        <div class="cart-item" data-id="${item.id}">
          <div class="cart-item-icon">
            <i class="fas ${iconClass}"></i>
          </div>
          <div class="cart-item-details">
            <div class="cart-item-name">${escapeHtml(item.name)}</div>
            <div class="cart-item-price">$${item.price.toFixed(2)}</div>
            <div class="cart-item-actions">
              <button class="qty-btn" data-action="decr" data-id="${item.id}">−</button>
              <span class="item-quantity">${item.quantity}</span>
              <button class="qty-btn" data-action="incr" data-id="${item.id}">+</button>
              <button class="remove-item" data-action="remove" data-id="${item.id}">Remove</button>
            </div>
          </div>
        </div>
      `;
    }).join('');
    
    // update total price
    const totalSpan = document.getElementById('cartTotalPrice');
    if (totalSpan) totalSpan.textContent = `$${getCartTotal().toFixed(2)}`;
    
    // attach event listeners to cart dynamic buttons
    document.querySelectorAll('.qty-btn').forEach(btn => {
      btn.addEventListener('click', (e) => {
        e.stopPropagation();
        const productId = parseInt(btn.getAttribute('data-id'));
        const action = btn.getAttribute('data-action');
        if (action === 'incr') updateQuantity(productId, 1);
        if (action === 'decr') updateQuantity(productId, -1);
      });
    });
    document.querySelectorAll('.remove-item').forEach(btn => {
      btn.addEventListener('click', (e) => {
        e.stopPropagation();
        const productId = parseInt(btn.getAttribute('data-id'));
        removeItemCompletely(productId);
      });
    });
  }

  // Cart sidebar open/close
  function openCart() {
    const overlay = document.getElementById('cartOverlay');
    if (overlay) overlay.classList.add('open');
    updateAllCartUI(); // refresh before show
  }
  function closeCart() {
    const overlay = document.getElementById('cartOverlay');
    if (overlay) overlay.classList.remove('open');
  }

  // Toast
  let toastTimeout;
  function showToast(message) {
    const toastEl = document.getElementById('toast');
    if (!toastEl) return;
    toastEl.textContent = message;
    toastEl.style.visibility = "visible";
    toastEl.style.opacity = "1";
    if (toastTimeout) clearTimeout(toastTimeout);
    toastTimeout = setTimeout(() => {
      toastEl.style.opacity = "0";
      setTimeout(() => { if(toastEl) toastEl.style.visibility = "hidden"; }, 300);
    }, 2000);
  }

  function escapeHtml(str) {
    return str.replace(/[&<>]/g, function(m) {
      if (m === '&') return '&amp;';
      if (m === '<') return '&lt;';
      if (m === '>') return '&gt;';
      return m;
    });
  }

  // filtering + product rendering
  let activeCategory = "all";
  let searchQuery = "";
  
  function getFilteredProducts() {
    let filtered = [...products];
    if (activeCategory !== "all") filtered = filtered.filter(p => p.category === activeCategory);
    if (searchQuery.trim()) {
      const q = searchQuery.trim().toLowerCase();
      filtered = filtered.filter(p => p.name.toLowerCase().includes(q));
    }
    return filtered;
  }
  
  function renderProducts() {
    const grid = document.getElementById('productsGrid');
    if (!grid) return;
    const filtered = getFilteredProducts();
    if (filtered.length === 0) {
      grid.innerHTML = `<div style="grid-column:1/-1; text-align:center; padding:60px;">🕶️ No products match.</div>`;
      return;
    }
    grid.innerHTML = filtered.map(p => {
      const iconClass = p.icon || "fa-bag-shopping";
      return `
        <div class="product-card">
          <div class="product-img"><i class="fas ${iconClass}" style="font-size: 3.5rem;"></i></div>
          <div class="product-info">
            <div class="product-title">${escapeHtml(p.name)}</div>
            <div class="product-category">${p.category}</div>
            <div class="price-row">
              <span class="current-price">$${p.price.toFixed(2)}</span>
              ${p.oldPrice ? `<span class="old-price">$${p.oldPrice.toFixed(2)}</span>` : ''}
            </div>
            <button class="add-to-cart" data-id="${p.id}"><i class="fas fa-shopping-cart"></i> Add to Cart</button>
          </div>
        </div>
      `;
    }).join('');
    document.querySelectorAll('.add-to-cart').forEach(btn => {
      btn.addEventListener('click', (e) => {
        const id = parseInt(btn.getAttribute('data-id'));
        addToCart(id);
      });
    });
  }
  
  function setActiveCategory(cat) {
    activeCategory = cat;
    document.querySelectorAll('.category-item').forEach(el => {
      if (el.getAttribute('data-cat') === cat) el.classList.add('active');
      else el.classList.remove('active');
    });
    renderProducts();
  }
  
  // event binding
  document.addEventListener('DOMContentLoaded', () => {
    loadCartFromLocal();
    renderProducts();
    document.querySelectorAll('.category-item').forEach(el => {
      el.addEventListener('click', () => setActiveCategory(el.getAttribute('data-cat')));
    });
    document.getElementById('searchBtn')?.addEventListener('click', () => {
      searchQuery = document.getElementById('searchInput')?.value || '';
      renderProducts();
    });
    document.getElementById('searchInput')?.addEventListener('keyup', (e) => {
      if (e.key === 'Enter') {
        searchQuery = e.target.value;
        renderProducts();
      }
    });
    document.querySelector('.hero-btn')?.addEventListener('click', () => showToast("✨ Summer collection unlocked! Use code: FRESH10"));
    document.querySelector('.view-all')?.addEventListener('click', () => {
      setActiveCategory('all');
      if(document.getElementById('searchInput')) document.getElementById('searchInput').value = '';
      searchQuery = '';
      renderProducts();
    });
    const cartTrigger = document.getElementById('cartIcon');
    if(cartTrigger) cartTrigger.addEventListener('click', openCart);
    document.getElementById('closeCartBtn')?.addEventListener('click', closeCart);
    document.getElementById('cartOverlay')?.addEventListener('click', (e) => {
      if(e.target === document.getElementById('cartOverlay')) closeCart();
    });
    document.getElementById('checkoutBtn')?.addEventListener('click', () => {
      if(cart.length) showToast(`✅ Checkout - Total $${getCartTotal().toFixed(2)} (demo)`);
      else showToast("Cart is empty");
    });
    updateAllCartUI();
  });
</script>
</body>
</html>