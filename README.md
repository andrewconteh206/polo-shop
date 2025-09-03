[inde.html](https://github.com/user-attachments/files/22106687/inde.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Drew Golden Finds | Shop</title>
  <meta name="description" content="Drew Golden Finds — Simple shop for men’s polos. Pay with AfriMoney or Orange Money in Sierra Leone." />
  <style>
    :root{
      --bg:#0f172a;
      --card:#111827;
      --muted:#94a3b8;
      --text:#e5e7eb;
      --brand:#f59e0b;
      --accent:#22c55e;
      --danger:#ef4444;
    }
    *{box-sizing:border-box}
    body{margin:0;font-family:Inter,system-ui,Segoe UI,Roboto,Helvetica,Arial,sans-serif;background:linear-gradient(180deg,#0b1225,#0f172a 20%,#0f172a 100%);color:var(--text)}
    a{color:var(--brand);text-decoration:none}
    header{position:sticky;top:0;background:rgba(17,24,39,.85);backdrop-filter:blur(8px);border-bottom:1px solid rgba(255,255,255,.06);z-index:10}
    .wrap{max-width:1040px;margin:0 auto;padding:16px}
    .row{display:flex;gap:16px;align-items:center;justify-content:space-between}
    .logo{display:flex;align-items:center;gap:10px}
    .brand{font-weight:800;letter-spacing:.3px}
    .badge{padding:4px 8px;border:1px solid rgba(255,255,255,.1);border-radius:999px;font-size:12px;color:var(--muted)}

    .hero{padding:48px 16px 24px}
    .hero-card{display:grid;grid-template-columns:1.2fr .8fr;gap:20px;background:linear-gradient(180deg,rgba(255,255,255,.03),rgba(255,255,255,.01));border:1px solid rgba(255,255,255,.06);border-radius:20px;padding:24px}
    .hero h1{font-size:28px;margin:0 0 6px}
    .hero p{margin:0;color:var(--muted)}
    .hero .highlight{color:var(--brand);font-weight:700}
    .hero img{width:100%;height:100%;object-fit:cover;border-radius:16px;border:1px solid rgba(255,255,255,.06)}

    .grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:16px}
    .card{background:var(--card);border:1px solid rgba(255,255,255,.08);border-radius:18px;padding:16px}
    .card h3{margin:0 0 6px;font-size:18px}
    .muted{color:var(--muted)}
    .price{font-weight:800}
    .btn{display:inline-flex;align-items:center;justify-content:center;gap:8px;padding:10px 14px;border-radius:12px;border:1px solid rgba(255,255,255,.1);background:rgba(255,255,255,.02);color:var(--text);cursor:pointer}
    .btn.primary{background:var(--brand);color:#111827;border-color:transparent;font-weight:800}
    .btn.full{width:100%}
    .btn.small{padding:8px 10px;font-size:14px;border-radius:10px}
    .btn:hover{filter:brightness(1.05)}

    .form{display:grid;gap:10px}
    label{font-size:12px;color:var(--muted)}
    input,select,textarea{width:100%;padding:12px;border-radius:12px;border:1px solid rgba(255,255,255,.12);background:#0b1220;color:var(--text)}
    input::placeholder,textarea::placeholder{color:#6b7280}

    .divider{height:1px;background:linear-gradient(90deg,rgba(255,255,255,0),rgba(255,255,255,.12),rgba(255,255,255,0));margin:16px 0}

    footer{padding:24px 16px;color:var(--muted);text-align:center}

    @media (max-width: 800px){
      .hero-card{grid-template-columns:1fr}
      .grid{grid-template-columns:1fr 1fr}
    }
  </style>
</head>
<body>
  <header>
    <div class="wrap row">
      <div class="logo">
        <svg width="28" height="28" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <path d="M5 12c0-3.866 3.134-7 7-7a7 7 0 1 1-7 7Z" stroke="currentColor" stroke-width="2"/>
          <path d="M12 5c2 4 4 6 8 7" stroke="currentColor" stroke-width="2"/>
        </svg>
        <div class="brand">Drew Golden Finds</div>
        <span class="badge">Sierra Leone • SLE</span>
      </div>
      <div class="row" style="gap:10px">
        <button class="btn small" id="viewOrder">View Order</button>
        <a href="#order" class="btn small primary">Checkout</a>
      </div>
    </div>
  </header>

  <section class="hero">
    <div class="wrap">
      <div class="hero-card">
        <div>
          <h1>Clean fits. <span class="highlight">Fair prices.</span></h1>
          <p>Shop men’s polos. Pay easily with <strong>AfriMoney</strong> or <strong>Orange Money</strong>. Fast delivery in Freetown and across Sierra Leone.</p>
          <div class="divider"></div>
          <div class="grid" id="products"></div>
        </div>
      </div>
    </div>
  </section>

  <section class='wrap' id='order' style='padding:8px 16px 24px'>
    <div class="grid">
      <div class="card">
        <h3>Checkout details</h3>
        <div class="divider"></div>
        <form class="form" id="checkoutForm">
          <div>
            <label for="fullName">Full name</label>
            <input id="fullName" name="fullName" placeholder="Your name" required />
          </div>
          <div>
            <label for="phone">Phone (WhatsApp)</label>
            <input id="phone" name="phone" placeholder="e.g. 07xxxxxxx or +2327xxxxxxx" required />
          </div>
          <div>
            <label for="address">Delivery address</label>
            <textarea id="address" name="address" placeholder="Street, area, city" rows="3" required></textarea>
          </div>
          <div>
            <label for="payment">Payment method</label>
            <select id="payment" name="payment" required>
              <option value="AfriMoney">AfriMoney</option>
              <option value="Orange Money">Orange Money</option>
            </select>
          </div>
          <button type="submit" class="btn primary full">Create Order & Payment Steps</button>
        </form>
      </div>

      <div class="card" id="summaryCard">
        <h3>Your order</h3>
        <div class="divider"></div>
        <div id="cartEmpty" class="muted">Your cart is empty. Add items above.</div>
        <div id="cartList" style="display:none"></div>
        <div class="divider"></div>
        <div class="row" style="justify-content:space-between"><div>Total</div><strong id="cartTotal">SLE 0</strong></div>
        <div id="orderResult" style="margin-top:12px;display:none"></div>
      </div>
    </div>
  </section>

  <footer>
    © <span id='year'></span> Drew Golden Finds · Pay with AfriMoney (077433848) or Orange Money (078259227)
  </footer>

  <script>
    const OWNER = {
      brand: 'Drew Golden Finds',
      afriMoney: '077433848',
      orangeMoney: '078259227',
      whatsappNumber: '077433848'
    };

    const cart = [];

    function addToCart(name, price){
      const found = cart.find(i => i.name === name);
      if(found){ found.qty += 1; } else { cart.push({name, price, qty:1}); }
      renderCart();
      scrollToSummary();
    }

    function renderCart(){
      const list = document.getElementById('cartList');
      const empty = document.getElementById('cartEmpty');
      const totalEl = document.getElementById('cartTotal');
      const orderResult = document.getElementById('orderResult');
      orderResult.style.display = 'none';
      if(cart.length === 0){
        list.style.display = 'none';
        empty.style.display = 'block';
        totalEl.textContent = 'SLE 0';
        return;
      }
      empty.style.display = 'none';
      list.style.display = 'block';
      list.innerHTML = cart.map((item, idx) => `
        <div class="row" style="justify-content:space-between;margin-bottom:6px">
          <div>${item.name} x${item.qty}</div>
          <div>SLE ${item.price*item.qty}</div>
        </div>
      `).join('');
      const total = cart.reduce((acc,i)=>acc+i.price*i.qty,0);
      totalEl.textContent = 'SLE ' + total;
    }

    function scrollToSummary(){document.getElementById('summaryCard').scrollIntoView({behavior:'smooth'});}

    document.getElementById('checkoutForm').addEventListener('submit', function(e){
      e.preventDefault();
      if(cart.length===0){alert('Add at least one item to cart'); return;}
      const name = document.getElementById('fullName').value;
      const phone = document.getElementById('phone').value;
      const address = document.getElementById('address').value;
      const payment = document.getElementById('payment').value;
      let msg = `Hello, I want to place this order:\n\nCustomer: ${name}\nPhone: ${phone}\nAddress: ${address}\nPayment: ${payment}\n\nOrder:\n`;
      cart.forEach(i=>{msg += `- ${i.name} x${i.qty} = SLE ${i.price*i.qty}\n`;});
      const total = cart.reduce((acc,i)=>acc+i.price*i.qty,0);
      msg += `\nTotal: SLE ${total}`;
      const waLink = `https://wa.me/${OWNER.whatsappNumber}?text=${encodeURIComponent(msg)}`;
      window.open(waLink, '_blank');
      document.getElementById('orderResult').style.display='block';
      document.getElementById('orderResult').innerHTML='Order sent! Check WhatsApp.';
    });

    document.getElementById('year').textContent = new Date().getFullYear();

    const poloImages = [
      'https://i.postimg.cc/MXQTJZNN/Whats-App-Image-2025-08-29-at-13-16-15-6bdd4712.jpg',
      'https://i.postimg.cc/gr8YBS6P/Whats-App-Image-2025-08-29-at-13-16-20-84d1e990.jpg',
      'https://i.postimg.cc/rDnct775/Whats-App-Image-2025-08-29-at-13-16-20-8d886175.jpg',
      'https://i.postimg.cc/HJrm0BCR/Whats-App-Image-2025-08-29-at-13-16-20-9a0d45e2.jpg',
      'https://i.postimg.cc/tsMQgWV5/Whats-App-Image-2025-08-29-at-13-16-23-00117f30.jpg',
      'https://i.postimg.cc/k24P9fDG/Whats-App-Image-2025-08-29-at-13-16-23-9cde6242.jpg',
      'https://i.postimg.cc/kBwPkkJL/Whats-App-Image-2025-08-29-at-13-16-23-d5fe8af8.jpg',
      'https://i.postimg.cc/DmPzwpfP/Whats-App-Image-2025-08-29-at-13-16-23-e57d47a2.jpg',
      'https://i.postimg.cc/Z9GG8mHv/Whats-App-Image-2025-08-29-at-13-16-24-0b4ee5c4.jpg',
      'https://i.postimg.cc/DmTZF3hz/Whats-App-Image-2025-08-29-at-13-16-24-53309bc9.jpg',
      'https://i.postimg.cc/SJQx2LJF/Whats-App-Image-2025-08-29-at-13-16-24-906957d4.jpg',
      'https://i.postimg.cc/dkKqqrzf/Whats-App-Image-2025-08-29-at-13-16-24-f301d361.jpg',
      'https://i.postimg.cc/gxQzTf4m/Whats-App-Image-2025-08-29-at-13-16-25-7346566a.jpg',
      'https://i.postimg.cc/14s9200n/Whats-App-Image-2025-08-29-at-13-16-25-d9785ec3.jpg',
      'https://i.postimg.cc/SnB4rcNK/Whats-App-Image-2025-08-29-at-13-16-25-ded2d0e0.jpg',
      'https://i.postimg.cc/5Y1Vc1zd/Whats-App-Image-2025-08-29-at-13-16-25-faeb1df9.jpg',
      'https://i.postimg.cc/8fzg5HwZ/Whats-App-Image-2025-08-29-at-13-16-26-5c108255.jpg',
      'https://i.postimg.cc/nMFJ0FZq/Whats-App-Image-2025-08-29-at-13-16-26-7aa0.jpg',
      'https://i.postimg.cc/Yq3FjR6v/Whats-App-Image-2025-08-29-at-13-16-26-xxxx.jpg',
      'https://i.postimg.cc/abcd1234/Whats-App-Image-2025-08-29-at-13-16-26-xxxx.jpg'
    ];

    const productsContainer = document.getElementById('products');
    for(let i=0; i<20; i++){
      const card = document.createElement('div');
      card.className = 'card';
      const imgSrc = poloImages[i];
      card.innerHTML = `
        <h3>Polo</h3>
        <img src='${imgSrc}' alt='Polo' style='width:100%;height:150px;object-fit:cover;border-radius:12px;margin-bottom:8px'/>
        <div class='muted'>Cotton pique</div>
        <div style='display:flex;gap:10px;align-items:center;justify-content:space-between;margin-top:8px'>
          <div>
            <div class='muted' style='font-size:12px'>Price</div>
            <div class='price' data-price='40'>SLE 40</div>
          </div>
          <button class='btn small' onclick="addToCart('Polo', 40)">Add to order</button>
        </div>
      `;
      productsContainer.appendChild(card);
    }
  </script>
</body>
</html>
