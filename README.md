<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Tienda - Tenis de shein- oferta por liquidación</title>
  <meta name="description" content="Ofertas reales de tenis. Pago seguro en OXXO mediante pasarela de pagos.">
  <style>
    /* Estilos base: edítalos libremente */
    :root{
      --maxW:1000px;
      --accent:#0b72ff;
      --muted:#777;
      --card:#fff;
      --bg:#f6f7fb;
    }
    body{font-family:Inter,system-ui,Arial,Helvetica,sans-serif;background:var(--bg);margin:0;padding:24px;display:flex;justify-content:center;}
    .wrap{max-width:var(--maxW);width:100%}
    header{display:flex;align-items:center;justify-content:space-between;margin-bottom:18px}
    header h1{margin:0;font-size:1.4rem}
    .grid{display:grid;grid-template-columns:1fr 360px;gap:18px}
    .card{background:var(--card);padding:16px;border-radius:10px;box-shadow:0 6px 18px rgba(15,20,30,0.06)}
    .product-row{display:flex;gap:14px;align-items:center}
    .product-row img{width:140px;height:140px;object-fit:cover;border-radius:8px}
    .price{font-weight:700;color:#111;font-size:1.15rem}
    .muted{color:var(--muted);font-size:0.9rem}
    button.btn{background:var(--accent);color:white;border:none;padding:10px 14px;border-radius:8px;cursor:pointer}
    button.btn:disabled{opacity:0.6;cursor:not-allowed}
    input,select,textarea{padding:10px;border:1px solid #e6e9ef;border-radius:8px;width:100%;box-sizing:border-box;margin-bottom:8px}
    .cart-item{display:flex;justify-content:space-between;align-items:center;padding:8px 0;border-bottom:1px dashed #eee}
    .voucher{background:#fff8e6;padding:12px;border-radius:8px;margin-top:12px;border:1px solid #f3e1b9}
    .small{font-size:0.85rem;color:var(--muted)}
    footer{text-align:center;color:var(--muted);margin-top:16px;font-size:0.9rem}
    @media(max-width:880px){ .grid{grid-template-columns:1fr} .product-row img{width:110px;height:110px} }
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <h1>Liquidación SHEIN</h1>
      <div class="small">Pago seguro | Envíos a todo México</div>
    </header>

    <div class="grid">
      <!-- COLUMNA PRINCIPAL: PRODUCTOS / DETALLES -->
      <div>
        <div class="card">
          <div class="product-row">
            <!--  -->
          <img src="https://img.ltwebstatic.com/images3_spmp/2024/08/03/8d/17226306575e31aae8af3c83cf2350f7b7fa7dfffa_thumbnail_750x999.jpg" alt="Logo de React">
            <div>
              <h2 id="productTitle">Tenis — Modelo Clásico</h2>
              <p class="muted" id="productDesc">Tenis cómodos y resistentes unisex.</p>
              <p class="price" id="productPrice">$49 MXN</p>
              <p class="small">Stock: <span id="productStock">98</span></p>

              <div style="margin-top:8px;">
                <label class="small">Talla</label>
                <select id="productSize" aria-label="Talla">
								  <option value="23">23</option>
                  <option value="25">25</option>
                  <option value="26">26</option>
                  <option value="27">27</option>
                  <option value="28">28</option>
                </select>
                <label class="small">Cantidad</label>
                <select id="productQty">
                  <option>1</option><option>2</option><option>3</option>
                </select>
                <div style="margin-top:10px;">
                  <button id="addCart" class="btn">Agregar al carrito</button>
                </div>
              </div>

            </div>
          </div>
        </div>

        <!-- SECCIÓN INFO / POLÍTICAS -->
        <div class="card" style="margin-top:12px;">
          <h3>Políticas</h3>
          <p class="small">Envíos: 2–7 días hábiles (según ubicación). Cambios y devoluciones dentro de 7 días con comprobante. Facturación disponible bajo solicitud.</p>
        </div>
      </div>

      <!-- COLUMNA DERECHA: CARRITO Y PAGO -->
      <aside>
        <div class="card">
          <h3>Carrito</h3>
          <div id="cartList" class="muted">Tu carrito está vacío</div>
          <div style="margin-top:10px;">
            <p class="small">Total: <strong id="cartTotal">$0</strong></p>
          </div>
        </div>

        <div class="card" style="margin-top:12px;">
          <h3>Datos de envío y pago</h3>

          <!-- IMPORTANTE: no almacenar claves privadas aquí. -->
          <input id="customerName" placeholder="Nombre completo" />
          <input id="customerEmail" placeholder="Correo electrónico" type="email" />
          <input id="customerPhone" placeholder="Teléfono" />
          <textarea id="customerAddress" placeholder="Dirección completa" rows="3"></textarea>

          <label class="small">Método de pago</label>
					<select id="paymentMethod">
    <option value="oxxo">Pagar en OXXO (Referencia: 5101257664722736)</option>
</select>
<p class="small">Transferencia OXXO o Spei: 5101257664722736 NU México</p> Enviar comprobante de pago con datos solicitados a los siguientes contactos 
+55 52332780
+55 52342123

          <div style="margin-top:10px;">
            <!--
              BOTÓN PRINCIPAL: hace POST a /api/create-order (tu backend)
              Tu backend debe:
                - Recibir items, total y datos cliente
                - Crear preference / cobro en MercadoPago o OpenPay usando claves privadas
                - Devolver { success: true, payment_url, voucher, order } en producción
            -->
          
          </div>

          <div id="paymentResult"></div>
          <div id="errors" class="small" style="color:#b00020"></div>
        </div>

        <div class="card" style="margin-top:12px;">
          <h4>Contacto</h4>
          <p class="small">WhatsApp: +52 5544098212</p>
          <p class="small">Correo: ventasporliquidacion@hotmail.com</p>
        </div>
      </aside>

    </div>

    <footer>
      <p>© <span id="year"></span> Tu tienda • Aviso de privacidad • Términos y condiciones</p>
    </footer>
  </div>

  <script>
    // --- Configurable: ENDPOINT de tu backend (producción) ---
    // Cambia esto por la URL pública de tu servidor, por ejemplo:
    // https://api.tudominio.com
    const BACKEND_BASE = 'https://tuservidor.com'; // <-- reemplaza por tu dominio/endpoint en producción

    // --- Estado simple del carrito ---
    const product = {
      id: 'tenis-xyz',
      title: document.getElementById('productTitle').innerText,
      price: 50,
      image: document.getElementById('productImage').src
    };
    let cart = [];

    document.getElementById('year').innerText = new Date().getFullYear();

    function renderCart(){
      const el = document.getElementById('cartList');
      if(!cart.length){
        el.innerHTML = '<div class="muted">Carrito vacío</div>';
        document.getElementById('cartTotal').innerText = '$0';
        return;
      }
      el.innerHTML = '';
      let total = 0;
      cart.forEach((it, idx) => {
        total += it.price * it.qty;
        const div = document.createElement('div');
        div.className = 'cart-item';
        div.innerHTML = `<div>
            <div style="font-weight:600">${it.title} <span class="small">talla ${it.size}</span></div>
            <div class="small">${it.qty} x $${it.price}</div>
          </div>
          <div>
            <button class="small" onclick="removeItem(${idx})">Eliminar</button>
          </div>`;
        el.appendChild(div);
      });
      document.getElementById('cartTotal').innerText = `$${total}`;
    }

    function removeItem(i){
      cart.splice(i,1);
      renderCart();
    }

    document.getElementById('addCart').addEventListener('click', ()=>{
      const size = document.getElementById('productSize').value;
      const qty = parseInt(document.getElementById('productQty').value,10);
      // simple control de stock
      const stock = parseInt(document.getElementById('productStock').innerText,10);
      if(qty > stock){
        alert('No hay suficiente stock');
        return;
      }
      // evitar duplicados (suma cantidades si misma talla)
      const exists = cart.find(c => c.id === product.id && c.size === size);
      if(exists) exists.qty += qty;
      else cart.push({ ...product, size, qty, price: product.price });
      renderCart();
    });

    // --- Pago: enviar al backend para que genere la orden / preferencia ---
    document.getElementById('payBtn').addEventListener('click', async ()=>{
      document.getElementById('errors').innerText = '';
      if(!cart.length){ document.getElementById('errors').innerText = 'Tu carrito está vacío.'; return; }

      const name = document.getElementById('customerName').value.trim();
      const email = document.getElementById('customerEmail').value.trim();
      const phone = document.getElementById('customerPhone').value.trim();
      const address = document.getElementById('customerAddress').value.trim();
      const paymentMethod = document.getElementById('paymentMethod').value;

      if(!name || !email || !phone || !address){ document.getElementById('errors').innerText = 'Completa todos los datos de envío.'; return; }

      // botón disabled para evitar doble envío
      const payBtn = document.getElementById('payBtn');
      payBtn.disabled = true;
      payBtn.innerText = 'Generando pedido…';

      const payload = {
        items: cart.map(i=>({ id:i.id, title:i.title, size:i.size, qty:i.qty, unit_price:i.price })),
        amount: cart.reduce((s,i)=>s + i.price * i.qty,0),
        customer: { name, email, phone, address },
        payment_method: paymentMethod // 'oxxo' o 'card'
      };

      try {
        // En producción BACKEND_BASE debe ser tu servidor seguro que usa claves privadas
        const res = await fetch(`${BACKEND_BASE}/api/create-order`, {
          method: 'POST',
          headers: { 'Content-Type':'application/json' },
          body: JSON.stringify(payload)
        });
        const data = await res.json();
        if(!res.ok || !data.success){
          document.getElementById('errors').innerText = data?.error || 'Error creando la orden. Revisa el servidor.';
          console.error(data);
        } else {
          // Respuesta esperada del backend (ejemplos):
          // - Para OXXO: { success:true, order:{...}, voucher:{reference,expires_at,barcode_url}, payment_url }
          // - Para tarjeta: { success:true, order:{...}, payment_url } (rediriges al checkout)
          const resultEl = document.getElementById('paymentResult');
          resultEl.innerHTML = '';
          if(data.payment_url){
            // Si la pasarela devuelve una URL (checkout), redirige o abre en nueva pestaña
            const a = document.createElement('a');
            a.href = data.payment_url;
            a.target = '_blank';
            a.rel = 'noopener';
            a.textContent = 'Abrir pasarela de pago';
            a.className = 'btn';
            resultEl.appendChild(a);
            // También muestra la info de la orden
            const pre = document.createElement('pre');
            pre.style.marginTop = '10px';
            pre.textContent = JSON.stringify(data.order, null, 2);
            resultEl.appendChild(pre);
          } else if (data.voucher){
            // Voucher OXXO — muestra referencia y/o PDF
            const v = data.voucher;
            const html = document.createElement('div');
            html.className = 'voucher';
            html.innerHTML = `<strong>Voucher OXXO</strong>
              <p>Referencia: <strong>${v.reference}</strong></p>
              <p>Vence: ${new Date(v.expires_at).toLocaleString()}</p>
              <p>Monto: <strong>$${data.order.amount} MXN</strong></p>
              ${v.barcode_url ? `<p><a href="${v.barcode_url}" target="_blank">Abrir voucher / código de barras (PDF)</a></p>` : ''}`;
            resultEl.appendChild(html);
          } else {
            resultEl.innerHTML = '<div class="small">Orden creada correctamente. Revisa tu panel de administrador para más detalles.</div>';
          }

          // Opcional: limpiar carrito y campos
          cart = [];
          renderCart();
        }
      } catch (err){
        console.error(err);
        document.getElementById('errors').innerText = 'Error de conexión con el servidor.';
      } finally {
        payBtn.disabled = false;
        payBtn.innerText = 'Proceder al pago';
      }
    });
  </script>
</body>
</html>
