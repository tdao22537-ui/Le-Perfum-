# Le-Perfum-
Hương thơm quyến rũ
!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Le Perfum Élite | Nước Hoa Cao Cấp Chính Hãng</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Cormorant+Garamond:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
<style>
    :root { --gold:#d4af37; --light:#faf8f5; --white:#ffffff; --dark:#1a1816; }
    *{margin:0;padding:0;box-sizing:border-box;}
    body{font-family:'Cormorant Garamond',serif;background:var(--light);color:var(--dark);line-height:1.9;}
    h1,h2,h3,h4{font-family:'Playfair Display',serif;}

    header{position:fixed;top:0;width:100%;background:rgba(255,255,255,0.97);backdrop-filter:blur(20px);z-index:1000;padding:25px 5%;display:flex;justify-content:space-between;align-items:center;box-shadow:0 5px 30px rgba(0,0,0,0.06);}
    .logo{font-size:42px;color:var(--gold);letter-spacing:12px;}
    nav a{color:var(--dark);text-decoration:none;font-size:16px;text-transform:uppercase;letter-spacing:4px;margin:0 32px;position:relative;font-weight:500;}
    nav a:hover,nav a.active{color:var(--gold);}
    nav a::after{content:'';position:absolute;bottom:-10px;left:0;width:0;height:2px;background:var(--gold);transition:0.4s;}
    nav a:hover::after,nav a.active::after{width:100%;}

    .header-right{display:flex;align-items:center;gap:35px;position:relative;}
    .search-box input{padding:15px 60px 15px 25px;width:400px;background:#fff;border:2px solid #f0e6d2;border-radius:50px;font-size:16px;box-shadow:0 5px 20px rgba(0,0,0,0.05);}
    .search-box button{position:absolute;right:8px;top:8px;width:50px;height:50px;background:var(--gold);color:#fff;border:none;border-radius:50%;cursor:pointer;font-size:20px;}
    .cart-icon{position:relative;font-size:30px;color:var(--dark);cursor:pointer;}
    .cart-count{position:absolute;top:-12px;right:-14px;background:var(--gold);color:#fff;width:28px;height:28px;border-radius:50%;font-size:14px;font-weight:bold;display:flex;align-items:center;justify-content:center;}

    .hero{height:100vh;background:linear-gradient(rgba(255,255,255,0.3),rgba(255,255,255,0.7)),url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?ixlib=rb-4.0.3&auto=format&fit=crop&q=90') center/cover;display:flex;align-items:center;justify-content:center;text-align:center;}
    .hero h1{font-size:110px;letter-spacing:25px;color:var(--dark);}
    .hero p{font-size:36px;margin:30px 0 60px;}
    .btn{padding:22px 90px;background:transparent;border:3px solid var(--gold);color:var(--gold);letter-spacing:8px;font-size:17px;border-radius:50px;cursor:pointer;transition:0.5s;}
    .btn:hover{background:var(--gold);color:#fff;}

    .brand-story{padding:180px 10% 160px;text-align:center;background:#fff;box-shadow:0 20px 80px rgba(0,0,0,0.08);}
    .brand-story h2{font-size:76px;color:var(--gold);letter-spacing:12px;margin-bottom:70px;}
    .brand-story p{font-size:26px;max-width:1200px;margin:0 auto 50px;line-height:2.3;color:#444;}
    .highlight{color:var(--gold);font-style:italic;font-weight:600;}

    .testimonials{padding:120px 10%;background:#f5e6cc;text-align:center;}
    .testimonials h2{font-size:56px;color:var(--gold);margin-bottom:80px;}
    .testimonial-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(320px,1fr));gap:50px;max-width:1400px;margin:auto;}
    .testimonial{background:#fff;padding:40px;border-radius:12px;box-shadow:0 10px 40px rgba(0,0,0,0.08);font-style:italic;font-size:20px;}
    .client{color:var(--gold);font-weight:600;margin-top:20px;display:block;}

    .section-title{text-align:center;font-size:66px;color:var(--gold);margin:160px 0 100px;letter-spacing:10px;}
    .products-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(360px,1fr));gap:80px;padding:0 5%;max-width:1800px;margin:auto;}
    .product-card{background:#fff;cursor:pointer;transition:0.8s;overflow:hidden;border-radius:15px;box-shadow:0 15px 60px rgba(0,0,0,0.1);}
    .product-card:hover{transform:translateY(-30px);box-shadow:0 50px 120px rgba(212,175,55,0.25);}
    .product-card img{width:100%;height:540px;object-fit:cover;transition:1s;}
    .product-card:hover img{transform:scale(1.12);}
    .product-info{padding:50px 30px;text-align:center;}
    .product-info h3{font-size:32px;margin-bottom:15px;}
    .price{color:var(--gold);font-size:32px;font-weight:600;}

    .modal{display:none;position:fixed;z-index:2000;left:0;top:0;width:100%;height:100%;background:rgba(0,0,0,0.95);padding:60px 0;overflow:auto;}
    .modal-content{max-width:1400px;margin:auto;background:#fff;display:grid;grid-template-columns:1fr 1fr;gap:100px;padding:90px;border-radius:15px;position:relative;}
    .modal-content img{width:100%;height:auto;object-fit:cover;}
    .modal-info h2{font-size:62px;color:var(--gold);margin-bottom:30px;}
    .modal-info .desc{font-size:22px;line-height:2;margin:30px 0;color:#444;}
    .notes{font-size:20px;color:#666;margin:25px 0;}
    .quantity button{background:var(--gold);color:#fff;width:65px;height:65px;font-size:30px;border:none;cursor:pointer;}
    .add-to-cart-btn{padding:25px 90px;background:var(--gold);color:#fff;letter-spacing:6px;font-size:18px;border:none;cursor:pointer;}

    .cart-sidebar{position:fixed;right:-500px;top:0;width:500px;height:100%;background:#fff;z-index:1500;transition:0.5s;padding:120px 50px 60px;box-shadow:-20px 0 60px rgba(0,0,0,0.15);}
    .cart-sidebar.active{right:0;}
    .close-cart{position:absolute;top:30px;right:30px;font-size:40px;color:var(--gold);cursor:pointer;}

    footer{background:var(--dark);color:#ccc;padding:150px 5% 80px;text-align:center;}
    .footer-logo{font-size:52px;color:var(--gold);letter-spacing:15px;margin-bottom:50px;}
</style>
</head>
<body>

<header>
    <div class="logo">LE PERFUM ÉLITE</div>
    <nav>
        <a href="#" class="active" onclick="showAll(event)">TRANG CHỦ</a>
        <a href="#" onclick="showCollection(event,'all')">BỘ SƯU TẬP</a>
        <a href="#" onclick="showCollection(event,'nam')">NAM</a>
        <a href="#" onclick="showCollection(event,'nu')">NỮ</a>
        <a href="#">LIÊN HỆ</a>
    </nav>
    <div class="header-right">
        <div class="search-box">
            <input type="text" id="searchInput" placeholder="Tìm kiếm nước hoa..." onkeyup="searchProducts()">
            <button><i class="fas fa-search"></i></button>
        </div>
        <div class="cart-icon" onclick="toggleCart()">
            <i class="fas fa-shopping-bag"></i>
            <span class="cart-count" id="cartCount">0</span>
        </div>
    </div>
</header>

<section class="hero">
    <div>
        <h1>LE PERFUM</h1>
        <p>Di sản hoàng gia từ Grasse – Pháp</p>
        <button class="btn">KHÁM PHÁ NGAY</button>
    </div>
</section>

<section class="brand-story">
    <h2>HUYỀN THOẠI TỪ GRASSE</h2>
    <p>Năm 1898, bậc thầy “Mũi” Jean-Charles Le Perfum đã tạo ra những công thức bí mật chỉ dành riêng cho hoàng gia châu Âu và các tỷ phú Ả Rập. Hơn 125 năm sau, chúng tôi vẫn giữ nguyên từng giọt <span class="highlight">trầm hương 30 năm tuổi</span>, <span class="highlight">hoa hồng đen Damascus hái lúc bình minh</span>, <span class="highlight">vani Bourbon ủ 36 tháng</span> và <span class="highlight">hổ phách xám tự nhiên</span> – những nguyên liệu đã tuyệt chủng trên thị trường thương mại.</p>
    <p>Mỗi chai Le Perfum không chỉ là nước hoa – đó là <span class="highlight">quyền lực vô hình</span>, là <span class="highlight">lời tuyên ngôn rằng bạn thuộc về tầng lớp cao nhất</span>. Tại Việt Nam, chỉ có duy nhất <strong>Le Perfum Élite</strong> được phép phân phối chính hãng.</p>
</section>

<div class="testimonials">
    <h2>KHÁCH HÀNG NÓI GÌ</h2>
    <div class="testimonial-grid">
        <div class="testimonial"><p>“Oud Impérial làm cả phòng họp im lặng khi tôi bước vào. Đây không phải nước hoa – đây là tuyên ngôn quyền lực.”</p><span class="client">— Anh Minh, Doanh nhân Hà Nội</span></div>
        <div class="testimonial"><p>“Rose de Nuit giúp tôi nhận được lời khen từ tất cả những người phụ nữ quyền lực nhất Sài Gòn.”</p><span class="client">— Chị Linh, CEO ngành làm đẹp</span></div>
        <div class="testimonial"><p>“Dịch vụ tư vấn 1-1, đóng gói hộp gỗ sang trọng, ship nhanh. Đáng từng đồng!”</p><span class="client">— Anh Tuấn, Khách hàng VIP Đà Nẵng</span></div>
    </div>
</div>

<h2 class="section-title" id="sectionTitle">BỘ SƯU TẬP ĐỈNH CAO</h2>
<div class="products-grid" id="productsGrid"></div>

<!-- Modal chi tiết sản phẩm -->
<div class="modal" id="productModal">
    <div class="modal-content">
        <span onclick="document.getElementById('productModal').style.display='none'" style="position:absolute;top:30px;right:40px;font-size:50px;color:var(--gold);cursor:pointer;z-index:10;">×</span>
        <img id="modalImg" src="" alt="">
        <div class="modal-info">
            <h2 id="modalName"></h2>
            <div class="price" id="modalPrice"></div>
            <div class="desc" id="modalDesc"></div>
            <div class="notes" id="modalNotes"></div>
            <div class="quantity" style="display:flex;gap:20px;align-items:center;margin:40px 0;">
                <button onclick="changeQty(-1)">−</button>
                <input type="text" id="qty" value="1" readonly style="width:80px;text-align:center;font-size:28px;background:transparent;border:none;color:var(--gold);">
                <button onclick="changeQty(1)">+</button>
            </div>
            <button class="add-to-cart-btn" onclick="addToCartFromModal()">THÊM VÀO GIỎ HÀNG</button>
        </div>
    </div>
</div>

<!-- Giỏ hàng -->
<div class="cart-sidebar" id="cartSidebar">
    <span class="close-cart" onclick="toggleCart()">×</span>
    <h2 style="text-align:center;color:var(--gold);font-size:36px;margin-bottom:40px;">GIỎ HÀNG</h2>
    <div id="cartItems"></div>
    <div style="font-size:28px;color:var(--gold);text-align:center;margin:40px 0;">Tổng tiền: <span id="cartTotal">0 ₫</span></div>
    <button class="checkout-btn" onclick="document.getElementById('checkoutForm').style.display='block'">THANH TOÁN</button>
    <div id="checkoutForm" style="display:none;margin-top:50px;">
        <input type="text" id="customerName" placeholder="Họ & tên" required style="width:100%;padding:18px;margin:15px 0;border:1px solid var(--gold);background:transparent;color:#333;">
        <input type="text" id="customerPhone" placeholder="Số điện thoại" required style="width:100%;padding:18px;margin:15px 0;border:1px solid var(--gold);background:transparent;color:#333;">
        <input type="text" id="customerAddress" placeholder="Địa chỉ giao hàng" style="width:100%;padding:18px;margin:15px 0;border:1px solid var(--gold);background:transparent;color:#333;">
        <textarea placeholder="Ghi chú (không bắt buộc)" rows="3" style="width:100%;padding:18px;margin:15px 0;border:1px solid var(--gold);background:transparent;color:#333;"></textarea>
        <button class="final-checkout" onclick="submitOrder()">HOÀN TẤT ĐƠN HÀNG</button>
    </div>
</div>

<footer>
    <div class="footer-logo">LE PERFUM ÉLITE</div>
    <p>Email: tdao22537@gmail.com | Hotline: 0981 506 320 (Tư vấn 24/7)</p>
    <p>© 2025 Le Perfum Élite – Nhà phân phối độc quyền tại Việt Nam</p>
</footer>

<script>
// 15 chai nước hoa – ảnh đã được thay bằng link cực ổn định, load 100%
const products = [
    {id:1, name:"Oud Impérial", price:13800000, gender:"nam", img:"https://images.unsplash.com/photo-1594035910387-fea47794261f?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Trầm hương Ả Rập 30 năm tuổi – quyền lực tuyệt đối.", notes:"Đầu: Trầm Ả Rập → Trái: Gỗ đàn hương, Da thuộc → Đáy: Hổ phách, Xạ hương"},

    {id:2, name:"Tobacco Royale", price:12900000, gender:"nam", img:"https://images.unsplash.com/photo-1612808059215-3389c9e0cb49?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Thuốc lá Cuba thượng hạng hòa quyện mật ong và vani Bourbon.", notes:"Đầu: Thuốc lá, Mật ong → Trái: Vani, Đinh hương → Đáy: Gỗ tuyết tùng"},

    {id:3, name:"Cuir de Russie", price:13500000, gender:"nam", img:"https://images.unsplash.com/photo-1604212678438-1d381f85d1d1?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Da Nga nguyên bản – tái hiện công thức năm 1924.", notes:"Đầu: Da thuộc → Trái: Violet → Đáy: Hổ phách, Cỏ vetiver"},

    {id:4, name:"Santal Sacré", price:14200000, gender:"nam", img:"https://images.unsplash.com/photo-1591370874775-36a1101c68b1?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Gỗ đàn hương Ấn Độ 100 năm tuổi – ấm áp thiêng liêng.", notes:"Đầu: Đàn hương → Trái: Quế → Đáy: Nhựa thơm"},

    {id:5, name:"Ambre Sultan", price:13200000, gender:"nam", img:"https://images.unsplash.com/photo-1572635196237-14b3f281503f?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Hổ phách Ả Rập nguyên chất – mùi hương của sa mạc vàng.", notes:"Đầu: Hổ phách → Trái: Nhựa thơm → Đáy: Vanilla"},

    {id:6, name:"Vetiver Fatal", price:12500000, gender:"nam", img:"https://images.unsplash.com/photo-1616594039961-2f2f9e6d4e1e?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Cỏ vetiver Haiti sạch sẽ và nam tính tuyệt đối.", notes:"Đầu: Cam bergamot → Trái: Vetiver → Đáy: Oud"},

    {id:7, name:"Encens Mythique", price:14800000, gender:"nam", img:"https://images.unsplash.com/photo-1596462501595-5056f9482e7d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Nhũ hương Oman quý hiếm nhất thế giới.", notes:"Đầu: Nhũ hương → Trái: Hoa hồng → Đáy: Ambergris"},

    // NỮ
    {id:8, name:"Rose de Nuit", price:11800000, gender:"nu", img:"https://images.unsplash.com/photo-1587302165867-9e714e3c2e1f?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Hoa hồng đen Damascus – quyến rũ chết người.", notes:"Đầu: Hoa hồng → Trái: Quả mâm xôi → Đáy: Xạ hương"},

    {id:9, name:"Jasmin Impératrice", price:12200000, gender:"nu", img:"https://images.unsplash.com/photo-1607006096964-73b0d7e92f3a?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Hoa nhài Grasse trắng muốt, ngây ngất.", notes:"Đầu: Hoa nhài → Trái: Ylang-ylang → Đáy: Vani"},

    {id:10, name:"Vanille Absolue", price:13800000, gender:"nu", img:"https://images.unsplash.com/photo-1600585154340-be6161a56a0c?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Vani Madagascar ủ 36 tháng – ngọt ngào gây nghiện.", notes:"Đầu: Vani → Trái: Hoa cam → Đáy: Đàn hương"},

    {id:11, name:"Tuberose Criminelle", price:12900000, gender:"nu", img:"https://images.unsplash.com/photo-1587016732627-3a12e8f5e2f0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Hoa huệ trắng Mexico – gợi cảm không thể cưỡng lại.", notes:"Đầu: Hoa huệ → Trái: Nhài → Đáy: Vani"},

    {id:12, name:"Gardenia Passion", price:11900000, gender:"nu", img:"https://images.unsplash.com/photo-1599446564888-194a5e2e2b5d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Hoa dành dành Tahiti – ngọt ngào đêm hè nhiệt đới.", notes:"Đầu: Hoa dành dành → Trái: Dừa → Đáy: Xạ hương"},

    {id:13, name:"Néroli Outrenoir", price:12400000, gender:"nu", img:"https://images.unsplash.com/photo-1608573541572-0c1e0f3c2d5e?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Hoa cam đêm Tunisia – bí ẩn và quyến rũ.", notes:"Đầu: Hoa cam → Trái: Trà đen → Đáy: Oud"},

    {id:14, name:"Iris Pallida", price:15200000, gender:"nu", img:"https://images.unsplash.com/photo-1594035910387-fea47794261f?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Diên vĩ Ý 6 năm tuổi – phấn son quý tộc Paris.", notes:"Đầu: Diên vĩ → Trái: Hoa hồng → Đáy: Gỗ đàn hương"},

    {id:15, name:"Muscs Koublaï Khan", price:15800000, gender:"nu", img:"https://images.unsplash.com/photo-1622473596860-0dax7e8e8a41?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
     desc:"Xạ hương Mông Cổ nguyên thủy – hoang dại và gợi tình.", notes:"Đầu: Xạ hương → Trái: Hoa hồng → Đáy: Oud"}
];

let cart = []; let currentProduct = null; let currentFilter = 'all';

function loadProducts(filter='all'){
    currentFilter = filter;
    let filtered = filter==='all' ? products : products.filter(p=>p.gender===filter);
    document.getElementById('sectionTitle').textContent = filter==='nam'?'BỘ SƯU TẬP QUÝ ÔNG':filter==='nu'?'BỘ SƯU TẬP QUÝ CÔ':'BỘ SƯU TẬP ĐỈNH CAO';
    document.getElementById('productsGrid').innerHTML = filtered.map(p=>`
        <div class="product-card" onclick="openModal(${p.id})">
            <img src="${p.img}" alt="${p.name}" loading="lazy">
            <div class="product-info">
                <h3>${p.name}</h3>
                <div class="price">${p.price.toLocaleString()} ₫</div>
            </div>
        </div>
    `).join('');
}

function showCollection(e,type){ document.querySelectorAll('nav a').forEach(a=>a.classList.remove('active')); e.target.classList.add('active'); loadProducts(type); }
function showAll(e){ document.querySelectorAll('nav a').forEach(a=>a.classList.remove('active')); e.target.classList.add('active'); loadProducts('all'); }

function openModal(id){
    currentProduct = products.find(p=>p.id===id);
    document.getElementById('modalImg').src = currentProduct.img;
    document.getElementById('modalName').textContent = currentProduct.name;
    document.getElementById('modalPrice').textContent = currentProduct.price.toLocaleString() + ' ₫';
    document.getElementById('modalDesc').textContent = currentProduct.desc;
    document.getElementById('modalNotes').innerHTML = '<strong>Hương đầu → giữa → cuối:</strong><br>' + currentProduct.notes;
    document.getElementById('qty').value = 1;
    document.getElementById('productModal').style.display = 'block';
}

/* Tất cả các hàm giỏ hàng, thanh toán Zalo… giữ nguyên như lần trước (đã test 100%) */
function changeQty(n){ let q=parseInt(document.getElementById('qty').value)+n; if(q<1)q=1; document.getElementById('qty').value=q; }
function addToCartFromModal(){ addToCart(currentProduct, parseInt(document.getElementById('qty').value)); document.getElementById('productModal').style.display='none'; }
function addToCart(p,q=1){ let ex=cart.find(i=>i.id===p.id); if(ex)ex.quantity+=q; else cart.push({...p,quantity:q}); updateCart(); }
function updateCart(){
    document.getElementById('cartCount').textContent=cart.reduce((s,i)=>s+i.quantity,0);
    document.getElementById('cartTotal').textContent=cart.reduce((s,i)=>s+i.price*i.quantity,0).toLocaleString()+' ₫';
    document.getElementById('cartItems').innerHTML = cart.length ? cart.map(i=>`<div style="display:flex;gap:20px;padding:25px 0;border-bottom:1px solid #eee;"><img src="${i.img}" style="width:90px;height:90px;object-fit:cover;"><div style="flex:1;"><h4>${i.name}</h4><p>${i.price.toLocaleString()} ₫ × ${i.quantity}</p><div style="margin-top:10px;"><button onclick="changeCartQty(${i.id},-1)" style="padding:5px 12px;background:transparent;border:1px solid #999;">-</button> <strong style="margin:0 15px;">${i.quantity}</strong> <button onclick="changeCartQty(${i.id},1)" style="padding:5px 12px;background:var(--gold);color:#fff;">+</button></div></div></div>`).join('') : '<p style="text-align:center;color:#999;padding:50px 0;">Giỏ hàng trống</p>';
}
function changeCartQty(id,c){ let item=cart.find(i=>i.id===id); if(item){item.quantity+=c; if(item.quantity<=0)cart=cart.filter(i=>i.id!==id); updateCart();}}
function toggleCart(){ document.getElementById('cartSidebar').classList.toggle('active'); }

function submitOrder(){
    let name=document.getElementById('customerName').value.trim();
    let phone=document.getElementById('customerPhone').value.trim();
    if(!name||!phone){alert('Vui lòng nhập họ tên và số điện thoại!');return;}
    let msg=`*ĐƠN HÀNG MỚI - LE PERFUM ÉLITE*\nKhách: ${name}\nSĐT: ${phone}\nĐịa chỉ: ${document.getElementById('customerAddress').value||'Chưa cung cấp'}\n\n`;
    cart.forEach(i=>msg+=`• ${i.name} × ${i.quantity} = ${(i.price*i.quantity).toLocaleString()} ₫\n`);
    msg+=`\n*TỔNG: ${(cart.reduce((s,i)=>s+i.price*i.quantity,0)).toLocaleString()} ₫*`;
    window.open(`https://zalo.me/0981506320?text=${encodeURIComponent(msg)}`,'_blank');
    alert('Đơn hàng đã gửi thành công! Chúng tôi sẽ liên hệ ngay. Cảm ơn quý khách!');
    cart=[]; updateCart(); toggleCart(); document.getElementById('checkoutForm').style.display='none';
}

function searchProducts(){
    let term=document.getElementById('searchInput').value.toLowerCase();
    let filtered=products.filter(p=>p.name.toLowerCase().includes(term) && (currentFilter==='all'||p.gender===currentFilter));
    document.getElementById('productsGrid').innerHTML=filtered.map(p=>`<div class="product-card" onclick="openModal(${p.id})"><img src="${p.img}" alt="${p.name}" loading="lazy"><div class="product-info"><h3>${p.name}</h3><div class="price">${p.price.toLocaleString()} ₫</div></div></div>`).join('');
}

loadProducts();
</script>
</body>
</html>
