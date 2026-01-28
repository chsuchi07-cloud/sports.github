<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>SportShop — Gear for Every Game</title>

  <!-- Google font -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

  <!-- Styles -->
  <link rel="stylesheet" href="styles.css" />
  <meta name="description" content="SportShop — shop shoes, apparel and equipment for football, basketball, running and more." />
</head>
<body>
  <header class="site-header">
    <div class="container header-inner">
      <a class="brand" href="#">SportShop</a>

      <form id="searchForm" class="search" role="search" aria-label="Search products">
        <input id="searchInput" type="search" placeholder="Search products, e.g. running shoes" aria-label="Search input" />
        <button type="submit" aria-label="Search">🔍</button>
      </form>

      <div class="header-actions">
        <nav class="main-nav" aria-label="Main">
          <a href="#" data-category="all" class="nav-link active">All</a>
          <a href="#" data-category="footwear" class="nav-link">Footwear</a>
          <a href="#" data-category="apparel" class="nav-link">Apparel</a>
          <a href="#" data-category="equipment" class="nav-link">Equipment</a>
        </nav>
        <button id="cartButton" class="cart-btn" aria-haspopup="dialog" aria-controls="cartPanel">
          🛒 <span id="cartCount" class="cart-count">0</span>
        </button>
      </div>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="container hero-inner">
        <div class="hero-text">
          <h1>Gear up. Play hard.</h1>
          <p>Top brands in footwear, apparel, and equipment — curated for athletes of all levels.</p>
          <a href="#products" class="btn-primary">Shop Featured</a>
        </div>
        <div class="hero-image" aria-hidden="true">
          <img src="https://images.unsplash.com/photo-1517649763962-0c623066013b?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=4e5a9103b8c8d5f9a8d64d6d3ff2f7aa" alt="" />
        </div>
      </div>
    </section>

    <section id="products" class="container products-section" aria-label="Products">
      <div class="section-header">
        <h2>Featured Products</h2>
        <div class="sort-filter">
          <label for="sortSelect">Sort:</label>
          <select id="sortSelect" aria-label="Sort products">
            <option value="featured">Featured</option>
            <option value="price-asc">Price — low to high</option>
            <option value="price-desc">Price — high to low</option>
          </select>
        </div>
      </div>

      <div id="productsGrid" class="products-grid" role="list"></div>

      <template id="productCardTemplate">
        <article class="product-card" role="listitem">
          <div class="thumb">
            <img src="" alt="" />
          </div>
          <div class="product-info">
            <h3 class="product-title"></h3>
            <p class="product-category"></p>
            <div class="price-row">
              <span class="price"></span>
              <button class="add-btn">Add to cart</button>
            </div>
          </div>
        </article>
      </template>
    </section>
  </main>

  <!-- Cart panel (simple modal) -->
  <div id="cartPanel" class="cart-panel" role="dialog" aria-modal="true" aria-hidden="true" aria-label="Shopping cart">
    <div class="cart-inner container">
      <button id="closeCart" class="close-cart" aria-label="Close cart">✕</button>
      <h3>Your Cart</h3>
      <ul id="cartList" class="cart-list" aria-live="polite"></ul>
      <div class="cart-footer">
        <div class="cart-total">Total: <strong id="cartTotal">$0.00</strong></div>
        <button id="checkoutBtn" class="btn-primary">Checkout</button>
      </div>
    </div>
  </div>

  <footer class="site-footer">
    <div class="container footer-inner">
      <p>© <span id="year"></span> SportShop — Built with ❤️</p>
      <nav class="footer-nav" aria-label="Footer">
        <a href="#">Contact</a>
        <a href="#">Returns</a>
        <a href="#">Privacy</a>
      </nav>
    </div>
  </footer>

  <script src="script.js" defer></script>
</body>
</html>
