<!DOCTYPE html>
<html lang="ms">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Western Test's Like Local - Menu</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: 'Segoe UI', Arial, sans-serif;
    background: #f8f9fa;
    color: #222;
    max-width: 900px;
    margin: 0 auto;
    padding-bottom: 100px;
  }

  /* TOP NAV BAR */
  .wft-navbar {
    background: #000;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    position: sticky;
    top: 0;
    z-index: 1000;
    border-bottom: 3px solid #da291c;
  }
  .nav-left {
    display: flex;
    align-items: center;
    gap: 16px;
  }

  /* LOGO B */
  .wft-logo-full {
    background: #000;
    color: #fff;
    padding: 6px 14px;
    border-radius: 8px;
    border-left: 4px solid #da291c;
    display: flex;
    flex-direction: column;
    line-height: 1;
    box-shadow: 0 2px 8px rgba(0,0,0,0.3);
  }
  .wft-text {
    font-family: 'Arial Black', sans-serif;
    font-size: 14px;
    font-weight: 900;
    letter-spacing: 1px;
  }
  .wft-sub {
    font-family: 'Arial', sans-serif;
    font-size: 9px;
    letter-spacing: 3px;
    color: #da291c;
    margin-top: 2px;
    font-weight: bold;
  }

  .nav-links {
    display: flex;
    gap: 15px;
    list-style: none;
    font-size: 14px;
    font-weight: 600;
  }
  .nav-links li {
    cursor: pointer;
    opacity: 0.9;
    transition: 0.2s;
    padding: 5px 8px;
    border-radius: 5px;
  }
  .nav-links li:hover {
    opacity: 1;
    background: rgba(218,41,28,0.3);
  }

  .nav-right {
    display: flex;
    align-items: center;
    gap: 15px;
  }
  .lang-btn-group {
    display: flex;
    background: rgba(255,255,255,0.15);
    border-radius: 15px;
    overflow: hidden;
  }
  .lang-btn-group button {
    background: transparent;
    border: none;
    color: white;
    padding: 5px 10px;
    font-size: 12px;
    font-weight: bold;
    cursor: pointer;
  }
  .lang-btn-group button.active {
    background: #da291c;
    color: white;
    border-radius: 15px;
  }

  .container { padding: 20px; }

  /* HERO BANNER */
  .hero-banner {
    background: linear-gradient(135deg, #000, #2a2a2a);
    color: white;
    border-radius: 12px;
    padding: 30px;
    text-align: center;
    margin-bottom: 24px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    border-left: 5px solid #da291c;
  }
  .hero-banner h1 { font-size: 26px; margin-bottom: 8px; color: #fff; }
  .hero-banner h1 span { color: #da291c; }
  .hero-banner p { font-size: 14px; opacity: 0.85; }

  h2.section-title {
    font-size: 20px;
    margin: 24px 0 12px;
    color: #000;
    border-bottom: 3px solid #da291c;
    padding-bottom: 6px;
    display: inline-block;
  }

  /* GRID MENU */
  .menu-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 16px;
    margin-top: 16px;
  }
  .menu-card {
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 2px 8px rgba(0,0,0,0.06);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    transition: 0.2s;
    border: 1px solid #eee;
  }
  .menu-card:hover { transform: translateY(-3px); box-shadow: 0 6px 15px rgba(0,0,0,0.12); border-color: #da291c; }
  .menu-img {
    width: 100%;
    height: 140px;
    object-fit: cover;
    background: #eee;
  }
  .menu-content { padding: 12px; display: flex; flex-direction: column; flex: 1; }
  .item-name { font-weight: bold; font-size: 14px; margin-bottom: 4px; color: #000; }
  .item-desc { font-size: 11px; color: #777; margin-bottom: 8px; flex: 1; }
  .card-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: auto;
  }
  .price { color: #da291c; font-weight: bold; font-size: 15px; }
  .order-btn {
    background: #000;
    color: white;
    border: none;
    padding: 6px 14px;
    border-radius: 20px;
    font-weight: bold;
    font-size: 12px;
    cursor: pointer;
    transition: 0.2s;
    border: 2px solid #000;
  }
  .order-btn:hover { background: #da291c; border-color: #da291c; }

  /* MERCHANDISE SECTION */
  .merch-section {
    margin-top: 30px;
    padding: 24px;
    background: linear-gradient(135deg, #000, #1a1a1a);
    border-radius: 16px;
    border-left: 5px solid #da291c;
    box-shadow: 0 4px 15px rgba(0,0,0,0.2);
  }
  .merch-section h2 {
    color: white;
    font-size: 22px;
    margin-bottom: 6px;
    border: none;
    display: block;
  }
  .merch-section h2 span { color: #da291c; }
  .merch-subtitle {
    color: #aaa;
    font-size: 13px;
    margin-bottom: 20px;
  }
  .merch-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
    gap: 14px;
  }
  .merch-card {
    background: #fff;
    border-radius: 12px;
    overflow: hidden;
    position: relative;
    transition: 0.3s;
    box-shadow: 0 2px 8px rgba(0,0,0,0.3);
  }
  .merch-card:hover {
    transform: translateY(-5px) scale(1.02);
    box-shadow: 0 8px 20px rgba(218,41,28,0.4);
  }
  .merch-img {
    width: 100%;
    height: 130px;
    object-fit: cover;
    background: #f0f0f0;
  }
  .merch-badge {
    position: absolute;
    top: 10px;
    right: 10px;
    background: #da291c;
    color: white;
    font-size: 10px;
    font-weight: bold;
    padding: 4px 10px;
    border-radius: 12px;
    letter-spacing: 1px;
    text-transform: uppercase;
    box-shadow: 0 2px 6px rgba(0,0,0,0.3);
    animation: pulse 2s infinite;
  }
  @keyframes pulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.05); }
  }
  .merch-content { padding: 10px 12px 12px; }
  .merch-name {
    font-weight: bold;
    font-size: 13px;
    color: #000;
    margin-bottom: 4px;
  }
  .merch-desc {
    font-size: 11px;
    color: #777;
    margin-bottom: 8px;
    min-height: 28px;
  }
  .merch-btn {
    width: 100%;
    padding: 8px;
    background: #000;
    color: white;
    border: none;
    border-radius: 6px;
    font-weight: bold;
    font-size: 11px;
    cursor: pointer;
    transition: 0.2s;
  }
  .merch-btn:hover { background: #da291c; }

  /* FLOATING CART */
  .cart-float-btn {
    position: fixed;
    bottom: 25px;
    right: 25px;
    background: #da291c;
    color: white;
    border: 3px solid #000;
    width: 65px;
    height: 65px;
    border-radius: 50%;
    font-size: 26px;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    cursor: pointer;
    z-index: 999;
    transition: 0.2s;
  }
  .cart-float-btn:hover { transform: scale(1.08); background: #b71c2c; }
  .cart-badge {
    position: absolute;
    top: -2px;
    right: -2px;
    background: #fff;
    color: #000;
    font-size: 12px;
    font-weight: bold;
    width: 24px;
    height: 24px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 2px solid #000;
  }

  /* CART MODAL */
  .modal {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.7);
    z-index: 2000;
    justify-content: center;
    align-items: flex-end;
  }
  .modal.open { display: flex; }
  .modal-content {
    background: white;
    width: 100%;
    max-width: 600px;
    max-height: 85vh;
    border-radius: 20px 20px 0 0;
    padding: 20px;
    overflow-y: auto;
    border-top: 4px solid #da291c;
  }
  .modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 2px solid #000;
    padding-bottom: 10px;
    margin-bottom: 15px;
    color: #000;
    font-size: 18px;
    font-weight: bold;
  }
  .close-modal { background: none; border: none; font-size: 24px; cursor: pointer; color: #777; }

  .cart-item-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 8px 0;
    border-bottom: 1px solid #f1f1f1;
    font-size: 14px;
  }
  .qty-box { display: flex; align-items: center; gap: 8px; }
  .qty-btn { width: 26px; height: 26px; border-radius: 50%; border: 1px solid #000; background: white; cursor: pointer; font-weight: bold; color: #000; }
  .qty-btn:hover { background: #000; color: white; }

  .total-section {
    display: flex;
    justify-content: space-between;
    font-size: 18px;
    font-weight: bold;
    margin: 15px 0;
    padding-top: 10px;
    border-top: 2px solid #000;
    color: #000;
  }
  .total-section #total-price-text { color: #da291c; }

  /* ORDER TYPE */
  .order-type-box {
    background: #f9f9f9;
    padding: 12px;
    border-radius: 8px;
    margin-bottom: 12px;
    border: 1px solid #e1e1e1;
    border-left: 3px solid #da291c;
  }
  .order-type-box label { display: block; font-size: 12px; font-weight: bold; margin-bottom: 8px; color: #000; }
  .order-type-options { display: flex; gap: 8px; flex-wrap: wrap; }
  .order-type-options button {
    flex: 1;
    min-width: 80px;
    padding: 10px 8px;
    border: 2px solid #ddd;
    background: white;
    border-radius: 8px;
    font-weight: bold;
    font-size: 12px;
    cursor: pointer;
    transition: 0.2s;
  }
  .order-type-options button.active { background: #000; color: white; border-color: #000; }
  .order-type-options button:hover { border-color: #da291c; }

  /* ADDRESS */
  .address-box {
    background: #f9f9f9;
    padding: 12px;
    border-radius: 8px;
    margin-bottom: 12px;
    border: 1px solid #e1e1e1;
    border-left: 3px solid #da291c;
    display: none;
  }
  .address-box.show { display: block; }
  .address-box label { display: block; font-size: 12px; font-weight: bold; margin-bottom: 4px; color: #000; }
  .address-box textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 6px;
    font-size: 13px;
    font-family: inherit;
    resize: vertical;
    min-height: 70px;
  }
  .address-box textarea:focus { outline: none; border-color: #da291c; box-shadow: 0 0 0 3px rgba(218,41,28,0.1); }

  /* CUSTOMER */
  .customer-box {
    background: #f9f9f9;
    padding: 12px;
    border-radius: 8px;
    margin-bottom: 12px;
    border: 1px solid #e1e1e1;
    border-left: 3px solid #da291c;
  }
  .customer-box label { display: block; font-size: 12px; font-weight: bold; margin-bottom: 4px; color: #000; }
  .customer-box input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 6px;
    font-size: 13px;
    margin-bottom: 8px;
  }
  .customer-box input:focus { outline: none; border-color: #da291c; box-shadow: 0 0 0 3px rgba(218,41,28,0.1); }

  /* BUTTONS */
  .action-checkout-btn {
    width: 100%;
    padding: 12px;
    background: #25D366;
    color: white;
    border: none;
    border-radius: 8px;
    font-weight: bold;
    font-size: 15px;
    cursor: pointer;
    margin-top: 5px;
  }
  .action-pay-btn { background: #da291c; margin-top: 8px; }
  .action-pay-btn:hover { background: #b71c2c; }

  .toast {
    position: fixed;
    bottom: 100px;
    left: 50%;
    transform: translateX(-50%) translateY(50px);
    background: #000;
    color: white;
    padding: 10px 20px;
    border-radius: 25px;
    font-size: 13px;
    opacity: 0;
    transition: 0.3s;
    pointer-events: none;
    z-index: 3000;
    border: 2px solid #da291c;
    max-width: 90%;
    text-align: center;
  }
  .toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }
</style>
</head>
<body>

  <!-- NAVBAR -->
  <div class="wft-navbar">
    <div class="nav-left">
      <div class="wft-logo-full">
        <span class="wft-text">WESTERN TEST'S</span>
        <span class="wft-sub">LIKE LOCAL</span>
      </div>
      <ul class="nav-links">
        <li onclick="scrollToSection('menu')" data-bm="Menu" data-en="Menu">Menu</li>
        <li onclick="scrollToSection('promosi')" data-bm="Promosi" data-en="Promotions">Promosi</li>
        <li onclick="scrollToSection('merchandise')" data-bm="Barangan" data-en="Merchandise">Barangan</li>
      </ul>
    </div>
    <div class="nav-right">
      <div class="lang-btn-group">
        <button id="btn-bm" class="active" onclick="setLang('bm')">BM</button>
        <button id="btn-en" onclick="setLang('en')">EN</button>
      </div>
    </div>
  </div>

  <div class="container">
    <!-- HERO / PROMOSI -->
    <div class="hero-banner" id="promosi">
      <h1 data-bm="Western Test's <span>Like Local</span>" data-en="Western Test's <span>Like Local</span>">Western Test's <span>Like Local</span></h1>
      <p data-bm="Rasa Western, Harga Local" data-en="Western Taste, Local Price">Rasa Western, Harga Local</p>
    </div>

    <!-- MENU -->
    <h2 class="section-title" id="menu" data-bm="Menu & Promosi Terkini" data-en="Latest Promotions & Menu">Menu & Promosi Terkini</h2>
    <div class="menu-grid" id="menu-container"></div>

    <!-- MERCHANDISE -->
    <div class="merch-section" id="merchandise">
      <h2 data-bm="Barangan <span>Eksklusif</span>" data-en="Exclusive <span>Merchandise</span>">Barangan <span>Eksklusif</span></h2>
      <p class="merch-subtitle" data-bm="Koleksi terhad - Akan datang tidak lama lagi!" data-en="Limited collection - Coming soon!">Koleksi terhad - Akan datang tidak lama lagi!</p>
      <div class="merch-grid" id="merch-container"></div>
    </div>
  </div>

  <button class="cart-float-btn" onclick="openCart()">
    🛒
    <span class="cart-badge" id="cart-badge">0</span>
  </button>

  <!-- CART MODAL -->
  <div class="modal" id="cart-modal" onclick="if(event.target===this)closeCart()">
    <div class="modal-content">
      <div class="modal-header">
        <span data-bm="Pesanan Troli Anda" data-en="Your Cart Order">Pesanan Troli Anda</span>
        <button class="close-modal" onclick="closeCart()">×</button>
      </div>
      <div id="cart-items-list"></div>
      <div class="total-section" id="total-section" style="display:none;">
        <span data-bm="Jumlah Keseluruhan:" data-en="Total Amount:">Jumlah Keseluruhan:</span>
        <span id="total-price-text">RM 0.00</span>
      </div>

      <!-- JENIS PESANAN -->
      <div class="order-type-box" id="order-type-box" style="display:none;">
        <label data-bm="Jenis Pesanan *" data-en="Order Type *">Jenis Pesanan *</label>
        <div class="order-type-options">
          <button type="button" onclick="setOrderType('pickup')" id="btn-pickup" data-bm="🏪 Ambil Sendiri" data-en="🏪 Pickup">🏪 Ambil Sendiri</button>
          <button type="button" onclick="setOrderType('delivery')" id="btn-delivery" data-bm="🛵 Penghantaran" data-en="🛵 Delivery">🛵 Penghantaran</button>
          <button type="button" onclick="setOrderType('cod')" id="btn-cod" data-bm="💵 COD" data-en="💵 COD">💵 COD</button>
        </div>
      </div>

      <!-- ALAMAT -->
      <div class="address-box" id="address-box">
        <label data-bm="Alamat Penghantaran *" data-en="Delivery Address *">Alamat Penghantaran *</label>
        <textarea id="cust-address" placeholder="Contoh: No 12, Jalan Merbau 3, Taman Merbau, 43000 Kajang, Selangor"></textarea>
      </div>

      <!-- MAKLUMAT PELANGGAN -->
      <div class="customer-box" id="customer-form" style="display:none;">
        <label data-bm="Nama Penuh *" data-en="Full Name *">Nama Penuh *</label>
        <input type="text" id="cust-name" placeholder="Contoh: Ahmad bin Ali">
        <label data-bm="Nombor Telefon *" data-en="Phone Number *">Nombor Telefon *</label>
        <input type="tel" id="cust-phone" placeholder="Contoh: 0194280014">
        <label data-bm="Emel (Pilihan)" data-en="Email (Optional)">Emel (Pilihan)</label>
        <input type="email" id="cust-email" placeholder="Contoh: ahmad@email.com">
      </div>

      <button class="action-checkout-btn" id="wa-btn" onclick="checkoutWhatsApp()" style="display:none;" data-bm="📱 Pesan Melalui WhatsApp" data-en="📱 Order via WhatsApp">📱 Pesan Melalui WhatsApp</button>
      <button class="action-checkout-btn action-pay-btn" id="pay-btn" onclick="bayarOnlineToyyib()" style="display:none;" data-bm="💳 Bayar Online (toyyibPay)" data-en="💳 Pay Online (toyyibPay)">💳 Bayar Online (toyyibPay)</button>
    </div>
  </div>

  <div class="toast" id="toast-msg"></div>

<script>
// ==========================================
// TETAPAN - TUKAR 3 BENDA DI SINI
// ==========================================
const WHATSAPP_NUMBER = "60194280014";
const TOYYIB_CATEGORY = "KOD_KATEGORI_ANDA";
const TOYYIB_SECRET   = "SECRET_KEY_ANDA";

let currentLang = 'bm';
let cart = {};
let orderType = null;

// ==========================================
// DATA MENU
// ==========================================
const MENU_DATA = [
  { id: "m1", price: 16.90, img: "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?w=400&q=80", bm: ["Set K-Spicy Burger", "Burger ayam pedas istimewa berserta kentang & minuman"], en: ["K-Spicy Burger Set", "Special spicy chicken burger with fries & drink"] },
  { id: "m2", price: 12.90, img: "https://images.unsplash.com/photo-1572802419224-296b0aeee0d9?w=400&q=80", bm: ["Set Filet-O-Fish", "Burger ikan lembut berserta sos tartar & kentang"], en: ["Filet-O-Fish Set", "Soft fish burger with tartar sauce & fries"] },
  { id: "m3", price: 15.90, img: "https://images.unsplash.com/photo-1562967914-608f82629710?w=400&q=80", bm: ["Set Beef Burger Deluxe", "Burger daging lembu juicy dengan keju cair"], en: ["Beef Burger Deluxe Set", "Juicy beef burger with melted cheese"] },
  { id: "m4", price: 17.90, img: "https://images.unsplash.com/photo-1606755962773-d324e0a13086?w=400&q=80", bm: ["Set Double Cheeseburger", "Dua lapis daging, dua lapis keju, puas hati"], en: ["Double Cheeseburger Set", "Double patty, double cheese, satisfying"] },
  { id: "m5", price: 19.90, img: "https://images.unsplash.com/photo-1626082927389-6cd097cdc6ec?w=400&q=80", bm: ["Set Ayam Goreng Rangup", "2 ketul ayam goreng rangup berempah + minuman"], en: ["Crispy Fried Chicken Set", "2 pieces of crispy spiced fried chicken + drink"] },
  { id: "m6", price: 22.90, img: "https://images.unsplash.com/photo-1562967916-eb82221dfb92?w=400&q=80", bm: ["Set Ayam Spicy Korean", "Ayam goreng bersalut sos pedas Korea"], en: ["Korean Spicy Chicken Set", "Fried chicken coated in Korean spicy sauce"] },
  { id: "m7", price: 11.90, img: "https://images.unsplash.com/photo-1562967916-eb82221dfb92?w=400&q=80", bm: ["Chicken Nuggets (6 pcs)", "Nuggets ayam rangup dengan sos pilihan"], en: ["Chicken Nuggets (6 pcs)", "Crispy chicken nuggets with choice of sauce"] },
  { id: "m8", price: 5.90, img: "https://images.unsplash.com/photo-1573080496219-bb080dd4f877?w=400&q=80", bm: ["Kentang Goreng (Fries)", "Kentang goreng panas rangup bermasin"], en: ["French Fries", "Hot crispy salted french fries"] },
  { id: "m9", price: 7.90, img: "https://images.unsplash.com/photo-1518013431117-eb1465fa5752?w=400&q=80", bm: ["Kentang Wedges Pedas", "Kentang wedges berempah dengan sos cheese"], en: ["Spicy Potato Wedges", "Spiced potato wedges with cheese sauce"] },
  { id: "m10", price: 8.90, img: "https://images.unsplash.com/photo-1639024471283-03518883512d?w=400&q=80", bm: ["Onion Rings Rangup", "Bawang goreng bersalut tepung rangup"], en: ["Crispy Onion Rings", "Crispy battered onion rings"] },
  { id: "m11", price: 6.90, img: "https://images.unsplash.com/photo-1563805042-7684c019e1cb?w=400&q=80", bm: ["McFlurry Oreo", "Ais krim vanilla dengan serpihan Oreo"], en: ["McFlurry Oreo", "Vanilla ice cream with Oreo crumbs"] },
  { id: "m12", price: 4.90, img: "https://images.unsplash.com/photo-1497034825429-c343d7c6a68f?w=400&q=80", bm: ["Sundae Coklat", "Ais krim vanilla dengan sos coklat"], en: ["Chocolate Sundae", "Vanilla ice cream with chocolate sauce"] },
  { id: "m13", price: 3.90, img: "https://images.unsplash.com/photo-1554866585-cd94860890b7?w=400&q=80", bm: ["Coca-Cola (Medium)", "Minuman berkarbonat sejuk"], en: ["Coca-Cola (Medium)", "Chilled carbonated drink"] },
  { id: "m14", price: 4.50, img: "https://images.unsplash.com/photo-1571934811356-5cc061b6821f?w=400&q=80", bm: ["Teh Tarik Kaw", "Teh tarik panas kaw style mamak"], en: ["Pulled Milk Tea", "Hot pulled milk tea mamak style"] },
  { id: "m15", price: 5.90, img: "https://images.unsplash.com/photo-1572490122747-3968b75cc699?w=400&q=80", bm: ["Iced Lemon Tea", "Teh lemon sejuk segar"], en: ["Iced Lemon Tea", "Refreshing cold lemon tea"] }
];

// ==========================================
// DATA MERCHANDISE
// ==========================================
const MERCH_DATA = [
  {
    id: "mc1",
    img: "https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?w=400&q=80",
    bm: ["T-Shirt Western Test's", "Cotton 100% - Design eksklusif"],
    en: ["Western Test's T-Shirt", "100% Cotton - Exclusive design"]
  },
  {
    id: "mc2",
    img: "https://images.unsplash.com/photo-1514228742587-6b1558fcca3d?w=400&q=80",
    bm: ["Mug Kopi WFT", "Ceramic mug 350ml - Tahan panas"],
    en: ["WFT Coffee Mug", "350ml ceramic mug - Heat resistant"]
  },
  {
    id: "mc3",
    img: "https://images.unsplash.com/photo-1588850561407-ed78c282e89b?w=400&q=80",
    bm: ["Cap Snapback WFT", "Adjustable - Satu saiz fit semua"],
    en: ["WFT Snapback Cap", "Adjustable - One size fits all"]
  },
  {
    id: "mc4",
    img: "https://images.unsplash.com/photo-1622560480605-d83c853bc5c3?w=400&q=80",
    bm: ["Keychain Logo WFT", "Metal keychain - Tahan lama"],
    en: ["WFT Logo Keychain", "Metal keychain - Durable"]
  }
];

// ==========================================
// RENDER MENU
// ==========================================
function renderMenu() {
  const container = document.getElementById("menu-container");
  container.innerHTML = MENU_DATA.map(item => `
    <div class="menu-card">
      <img src="${item.img}" class="menu-img" alt="${item[currentLang][0]}" onerror="this.src='https://via.placeholder.com/300x200?text=Food'">
      <div class="menu-content">
        <div class="item-name">${item[currentLang][0]}</div>
        <div class="item-desc">${item[currentLang][1]}</div>
        <div class="card-footer">
          <span class="price">RM ${item.price.toFixed(2)}</span>
          <button class="order-btn" onclick="addToCart('${item.id}')" data-bm="Pilih" data-en="Order">Pilih</button>
        </div>
      </div>
    </div>
  `).join("");
  updateTexts();
}

// ==========================================
// RENDER MERCHANDISE
// ==========================================
function renderMerch() {
  const container = document.getElementById("merch-container");
  container.innerHTML = MERCH_DATA.map(item => `
    <div class="merch-card">
      <span class="merch-badge" data-bm="Coming Soon" data-en="Coming Soon">Coming Soon</span>
      <img src="${item.img}" class="merch-img" alt="${item[currentLang][0]}" onerror="this.src='https://via.placeholder.com/300x200?text=Merch'">
      <div class="merch-content">
        <div class="merch-name">${item[currentLang][0]}</div>
        <div class="merch-desc">${item[currentLang][1]}</div>
        <button class="merch-btn" onclick="notifyMe('${item[currentLang][0]}')" data-bm="🔔 Beritahu Saya" data-en="🔔 Notify Me">🔔 Beritahu Saya</button>
      </div>
    </div>
  `).join("");
  updateTexts();
}

// ==========================================
// NOTIFY ME
// ==========================================
function notifyMe(itemName) {
  const msg = currentLang === 'bm'
    ? `*BERITAHU SAYA - MERCHANDISE*%0A%0ASaya berminat dengan: *${itemName}*%0A%0ATolong beritahu saya bila available!`
    : `*NOTIFY ME - MERCHANDISE*%0A%0AI'm interested in: *${itemName}*%0A%0APlease notify me when available!`;
  window.open(`https://wa.me/${WHATSAPP_NUMBER}?text=${msg}`, "_blank");
  showToast(currentLang === 'bm' ? "Membuka WhatsApp..." : "Opening WhatsApp...");
}

// ==========================================
// SCROLL FUNCTIONS
// ==========================================
function scrollToSection(id) {
  const el = document.getElementById(id);
  if (el) {
    el.scrollIntoView({ behavior: 'smooth', block: 'start' });
    closeCart();
  }
}

// ==========================================
// ORDER TYPE
// ==========================================
function setOrderType(type) {
  orderType = type;
  document.getElementById("btn-pickup").classList.remove("active");
  document.getElementById("btn-delivery").classList.remove("active");
  document.getElementById("btn-cod").classList.remove("active");

  if (type === 'pickup') document.getElementById("btn-pickup").classList.add("active");
  if (type === 'delivery') document.getElementById("btn-delivery").classList.add("active");
  if (type === 'cod') document.getElementById("btn-cod").classList.add("active");

  const addressBox = document.getElementById("address-box");
  if (type === 'pickup') {
    addressBox.classList.remove("show");
  } else {
    addressBox.classList.show ? null : addressBox.classList.add("show");
  }
}

// ==========================================
// CART
// ==========================================
function findItem(id) { return MENU_DATA.find(i => i.id === id); }

function addToCart(id) {
  cart[id] = (cart[id] || 0) + 1;
  updateBadge();
  const item = findItem(id);
  showToast((currentLang === 'bm' ? "Berjaya menambah: " : "Successfully added: ") + item[currentLang][0]);
}

function updateBadge() {
  const totalItems = Object.values(cart).reduce((a, b) => a + b, 0);
  document.getElementById("cart-badge").textContent = totalItems;
}

function openCart() {
  renderCartModal();
  document.getElementById("cart-modal").classList.add("open");
}

function closeCart() {
  document.getElementById("cart-modal").classList.remove("open");
}

function renderCartModal() {
  const listEl = document.getElementById("cart-items-list");
  const keys = Object.keys(cart);

  if (keys.length === 0) {
    listEl.innerHTML = `<div style="text-align:center; padding:30px; color:#777;" data-bm="Troli anda masih kosong." data-en="Your cart is empty.">Troli anda masih kosong.</div>`;
    document.getElementById("total-section").style.display = "none";
    document.getElementById("order-type-box").style.display = "none";
    document.getElementById("address-box").classList.remove("show");
    document.getElementById("customer-form").style.display = "none";
    document.getElementById("wa-btn").style.display = "none";
    document.getElementById("pay-btn").style.display = "none";
    updateTexts();
    return;
  }

  let total = 0;
  listEl.innerHTML = keys.map(id => {
    const item = findItem(id);
    const qty = cart[id];
    const sub = item.price * qty;
    total += sub;
    return `
      <div class="cart-item-row">
        <div>
          <strong>${item[currentLang][0]}</strong><br>
          <span style="color:#da291c; font-size:12px;">RM ${item.price.toFixed(2)} × ${qty} = RM ${sub.toFixed(2)}</span>
        </div>
        <div class="qty-box">
          <button class="qty-btn" onclick="changeQty('${id}', -1)">-</button>
          <span>${qty}</span>
          <button class="qty-btn" onclick="changeQty('${id}', 1)">+</button>
        </div>
      </div>
    `;
  }).join("");

  document.getElementById("total-price-text").textContent = "RM " + total.toFixed(2);
  document.getElementById("total-section").style.display = "flex";
  document.getElementById("order-type-box").style.display = "block";
  document.getElementById("customer-form").style.display = "block";
  document.getElementById("wa-btn").style.display = "block";
  document.getElementById("pay-btn").style.display = "block";
  updateTexts();
}

function changeQty(id, delta) {
  cart[id] = (cart[id] || 0) + delta;
  if (cart[id] <= 0) delete cart[id];
  updateBadge();
  renderCartModal();
}

// ==========================================
// VALIDASI
// ==========================================
function validateForm() {
  const name = document.getElementById("cust-name").value.trim();
  const phone = document.getElementById("cust-phone").value.trim();

  if (!name || !phone) {
    showToast(currentLang === 'bm' ? "Sila isi Nama dan Nombor Telefon!" : "Please fill in Name and Phone Number!");
    return null;
  }

  if (!orderType) {
    showToast(currentLang === 'bm' ? "Sila pilih jenis pesanan!" : "Please select order type!");
    return null;
  }

  const address = document.getElementById("cust-address").value.trim();
  if ((orderType === 'delivery' || orderType === 'cod') && !address) {
    showToast(currentLang === 'bm' ? "Sila isi alamat penghantaran!" : "Please fill in delivery address!");
    return null;
  }

  return { name, phone, email: document.getElementById("cust-email").value.trim(), address };
}

// ==========================================
// CHECKOUT WHATSAPP
// ==========================================
function checkoutWhatsApp() {
  const cust = validateForm();
  if (!cust) return;

  let msg = currentLang === 'bm' ? "*PESANAN BARU - WESTERN TEST'S LIKE LOCAL*%0A%0A" : "*NEW ORDER - WESTERN TEST'S LIKE LOCAL*%0A%0A";
  msg += `Nama: ${cust.name}%0A`;
  msg += `Telefon: ${cust.phone}%0A`;
  msg += `Jenis: ${orderType === 'pickup' ? '🏪 Ambil Sendiri' : orderType === 'delivery' ? '🛵 Penghantaran' : '💵 COD'}%0A`;
  if (cust.address) msg += `Alamat: ${cust.address}%0A`;
  msg += `%0A`;

  let total = 0;
  Object.keys(cart).forEach(id => {
    const item = findItem(id);
    const q = cart[id];
    const sub = item.price * q;
    total += sub;
    msg += `• ${item[currentLang][0]} x ${q} = RM ${sub.toFixed(2)}%0A`;
  });
  msg += `%0A*Jumlah: RM ${total.toFixed(2)}*`;

  window.open(`https://wa.me/${WHATSAPP_NUMBER}?text=${msg}`, "_blank");
}

// ==========================================
// BAYAR ONLINE (TOYYIBPAY)
// ==========================================
function bayarOnlineToyyib() {
  const cust = validateForm();
  if (!cust) return;

  let total = 0;
  let desc = "";
  Object.keys(cart).forEach(id => {
    const item = findItem(id);
    const q = cart[id];
    total += item.price * q;
    desc += item[currentLang][0] + " (" + q + "), ";
  });

  desc += " | " + (orderType === 'pickup' ? 'Pickup' : orderType === 'delivery' ? 'Delivery' : 'COD');
  if (cust.address) desc += " - " + cust.address.substring(0, 50);

  showToast(currentLang === 'bm' ? "Menghubungkan ke ToyyibPay..." : "Connecting to ToyyibPay...");

  const params = new URLSearchParams();
  params.append("userSecretKey", TOYYIB_SECRET);
  params.append("categoryCode", TOYYIB_CATEGORY);
  params.append("billName", "Order Western Test's");
  params.append("billDescription", desc);
  params.append("billPriceSetting", "1");
  params.append("billPayorInfo", "1");
  params.append("billAmount", Math.round(total * 100));
  params.append("billReturnUrl", window.location.href);
  params.append("billCallbackUrl", window.location.href);
  params.append("billExternalReferenceNo", "WFT" + Date.now());
  params.append("billTo", cust.name);
  params.append("billEmail", cust.email || "test@email.com");
  params.append("billPhone", cust.phone);
  params.append("billSplitPayment", "0");
  params.append("billPaymentChannel", "0");
  params.append("billChargeToCustomer", "1");

  fetch("https://toyyibpay.com/index.php/api/createBill", { method: "POST", body: params })
    .then(res => res.json())
    .then(data => {
      if (data[0] && data[0].BillCode) {
        window.location.href = "https://toyyibpay.com/" + data[0].BillCode;
      } else {
        showToast("Ralat API ToyyibPay.");
      }
    }).catch(() => showToast("Gagal menyambung ke pelayan pembayaran."));
}

// ==========================================
// TOAST
// ==========================================
function showToast(text) {
  const t = document.getElementById("toast-msg");
  t.textContent = text;
  t.classList.add("show");
  setTimeout(() => t.classList.remove("show"), 2500);
}

// ==========================================
// SET LANGUAGE
// ==========================================
function setLang(lang) {
  currentLang = lang;
  document.getElementById("btn-bm").classList.toggle("active", lang === 'bm');
  document.getElementById("btn-en").classList.toggle("active", lang === 'en');
  renderMenu();
  renderMerch();
  if (document.getElementById("cart-modal").classList.contains("open")) {
    renderCartModal();
  }
}

function updateTexts() {
  document.querySelectorAll("[data-bm]").forEach(el => {
    if (el.innerHTML.includes('<span>')) return;
    el.textContent = el.getAttribute("data-" + currentLang);
  });
}

// ==========================================
// START
// ==========================================
renderMenu();
renderMerch();
updateBadge();
</script>
</body>
</html>
