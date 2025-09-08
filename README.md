<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Aguada de Pablo Atlántico</title>
  <meta name="description" content="Sitio web informativo de Aguada de Pablo, corregimiento de Sabanalarga (Atlántico, Colombia): historia, cultura, turismo y servicios locales." />
  <meta property="og:title" content="Aguada de Pablo – Sabanalarga, Atlántico" />
  <meta property="og:description" content="Historia, cultura, turismo y servicios de Aguada de Pablo." />
  <meta property="og:type" content="website" />
  <meta name="theme-color" content="#174EA6" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --azul:#1e90ff;     /* azul celeste simbólico */
      --azul-osc:#174EA6; /* acento */
      --blanco:#ffffff;   /* blanco simbólico */
      --rojo:#e53935;     /* rojo simbólico */
      --dorado:#c9a227;   /* acento opcional para escudo */
      --gris:#2c3e50;
      --gris-suave:#f5f7fb;
      --sombra:0 10px 30px rgba(0,0,0,.08);
      --radio:20px;
    }
    html,body{margin:0;font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;color:#172026;background:var(--gris-suave);} 
    a{color:var(--azul-osc);text-decoration:none}
    img{max-width:100%;display:block}
    .contenedor{width:min(1100px,92%);margin:auto}
    /* Header */
    header{position:sticky;top:0;z-index:50;background:rgba(255,255,255,.85);backdrop-filter:saturate(180%) blur(10px);border-bottom:1px solid rgba(0,0,0,.06)}
    .nav{display:flex;align-items:center;justify-content:space-between;padding:10px 0}
    .marca{display:flex;gap:10px;align-items:center}
    .marca__escudo{width:42px;height:42px;border-radius:12px;background:linear-gradient(135deg,var(--azul),var(--blanco),var(--rojo));box-shadow:inset 0 0 0 3px rgba(255,255,255,.7), 0 6px 16px rgba(0,0,0,.15);position:relative;overflow:hidden}
    .marca__escudo:before{content:"";position:absolute;inset:6px;border-radius:10px;border:3px solid var(--blanco)}
    .marca__texto{font-weight:800;letter-spacing:.3px}
    nav ul{display:flex;gap:16px;list-style:none;margin:0;padding:0}
    nav a{padding:8px 12px;border-radius:12px;font-weight:600}
    nav a:hover{background:rgba(30,144,255,.12)}
    .cta{background:var(--azul-osc);color:white;padding:10px 14px;border-radius:14px}
    .cta:hover{opacity:.9}

    /* Hero */
    .hero{position:relative;overflow:hidden;background:linear-gradient(180deg, rgba(23,78,166,0.8), rgba(30,144,255,0.8)), url('https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?q=80&w=1600&auto=format&fit=crop') center/cover;}
    .hero__inner{display:grid;grid-template-columns:1.2fr .8fr;gap:24px;align-items:center;min-height:72vh;padding:64px 0;color:white}
    .hero h1{font-size:clamp(28px,4vw,54px);line-height:1.05;margin:0 0 10px}
    .hero p{font-size:clamp(16px,2.2vw,20px);opacity:.95}
    .hero__tarjeta{background:white;color:#172026;border-radius:var(--radio);box-shadow:var(--sombra);padding:20px}
    .hero__chips{display:flex;flex-wrap:wrap;gap:10px;margin:16px 0 0}
    .chip{border:1px solid rgba(0,0,0,.08);padding:8px 12px;border-radius:999px;background:#fff;font-weight:600}

    /* Secciones */
    section{padding:64px 0}
    .titulo{font-size:clamp(24px,3vw,34px);margin:0 0 14px}
    .sub{color:#4b5563;margin:0 0 26px}

    /* Tarjetas */
    .grid{display:grid;gap:20px}
    .grid-3{grid-template-columns:repeat(3,1fr)}
    .grid-2{grid-template-columns:repeat(2,1fr)}
    @media (max-width:980px){.hero__inner{grid-template-columns:1fr}.grid-3{grid-template-columns:1fr 1fr}.grid-2{grid-template-columns:1fr}}
    @media (max-width:640px){.grid-3{grid-template-columns:1fr}}

    .card{background:white;border-radius:var(--radio);box-shadow:var(--sombra);overflow:hidden;border:1px solid rgba(0,0,0,.06)}
    .card__caja{padding:18px}
    .badge{display:inline-flex;align-items:center;gap:8px;background:linear-gradient(90deg,var(--azul), var(--rojo));color:white;padding:8px 12px;border-radius:999px;font-weight:700;font-size:12px;letter-spacing:.3px}

    /* Línea de tiempo */
    .timeline{position:relative;padding-left:20px}
    .timeline:before{content:"";position:absolute;left:10px;top:0;bottom:0;width:3px;background:linear-gradient(var(--azul),var(--rojo))}
    .item{position:relative;margin:16px 0 0 10px;padding:14px 14px 14px 18px;background:white;border-radius:14px;border-left:4px solid var(--azul);box-shadow:var(--sombra)}
    .item:before{content:"";position:absolute;left:-16px;top:20px;width:12px;height:12px;background:var(--azul);border:3px solid white;border-radius:50%;box-shadow:0 0 0 3px rgba(30,144,255,.2)}

    /* Franja tricolor */
    .franja{height:10px;background:linear-gradient(90deg,var(--azul),var(--blanco),var(--rojo))}

    /* Footer */
    footer{background:#111827;color:#cbd5e1;padding:38px 0;margin-top:20px}
    .footer-grid{display:grid;gap:18px;grid-template-columns:2fr 1fr 1fr}
    @media(max-width:900px){.footer-grid{grid-template-columns:1fr}}
    .footbrand{display:flex;align-items:center;gap:12px}
    .pill{display:inline-block;background:#0b1220;color:white;border-radius:999px;padding:6px 12px;font-size:12px;font-weight:700;letter-spacing:.3px}

    /* Botón flotante */
    .float{
      position:fixed;right:18px;bottom:18px;background:var(--rojo);color:white;border:none;border-radius:999px;padding:12px 16px;font-weight:800;box-shadow:var(--sombra);cursor:pointer
    }
    .float:hover{filter:brightness(1.05)}

    /* Tabla simple */
    table{width:100%;border-collapse:collapse}
    th,td{padding:12px;border-bottom:1px solid #e5e7eb;text-align:left}
    th{background:#f1f5f9}
  </style>
</head>
<body>
  <header>
    <div class="contenedor nav">
      <div class="marca">
        <div class="marca__escudo" aria-hidden="true"></div>
        <div class="marca__texto">Aguada de Pablo</div>
      </div>
      <nav aria-label="principal">
        <ul>
          <li><a href="#inicio">Inicio</a></li>
          <li><a href="#historia">Historia</a></li>
          <li><a href="#cultura">Cultura</a></li>
          <li><a href="#turismo">Turismo</a></li>
          <li><a href="#directorio">Directorio</a></li>
          <li><a class="cta" href="#contacto">Contactar</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main id="inicio" class="hero">
    <div class="contenedor hero__inner">
      <div>
        <span class="badge" aria-label="Colores y símbolo">Aguada de Pablo · Azul · Blanco · Rojo · Pivijay</span>
        <h1>Un pueblo con río, embalse y corazón caribe</h1>
        <p>
          Aguada de Pablo es un corregimiento de <strong>Sabanalarga, Atlántico</strong>. Con raíces coloniales, vínculos con el río y el <strong>Embalse del Guájaro</strong>,
          tradición pesquera y un carácter alegre que nos une.
        </p>
        <div class="hero__chips" role="list">
          <span class="chip" role="listitem">Educación y unidad</span>
          <span class="chip" role="listitem">Pueblo pesquero</span>
          <span class="chip" role="listitem">Árbol de Pivijay</span>
        </div>
      </div>
      <aside class="hero__tarjeta" aria-label="Información rápida">
        <h3 style="margin:0 0 10px">Información rápida</h3>
        <table>
          <tr><th>Municipio</th><td>Sabanalarga (Atlántico)</td></tr>
          <tr><th>Gentilicio</th><td>Aguadapableros</td></tr>
          <tr><th>Actividades</th><td>Pesca artesanal, comercio local, agricultura</td></tr>
          <tr><th>Colores representativos</th><td>Colores azul rey, blanco y rojo · Árbol de Ceiba</td></tr>
          <tr><th>Declaración</th><td> Alexandra te amoooo att Nayith</th><td>
        </table>
        <p style="margin:10px 0 0;font-size:14px;color:#475569">
          *Contenido editable; agrega datos oficiales cuando los tengas.
        </p>
      </aside>
    </div>
    <div class="franja" aria-hidden="true"></div>
  </main>

  <section id="historia">
    <div class="contenedor">
      <h2 class="titulo">Historia y raíces</h2>
      <p class="sub">Una línea de tiempo breve con los hitos más representativos del corregimiento.</p>
      <div class="timeline">
        <div class="item">
          <strong>Época colonial</strong>
          <p>Origen vinculado a rutas fluviales y a la riqueza hídrica; se consolidan asentamientos cercanos al río.</p>
        </div>
        <div class="item">
          <strong>Conexión con el Embalse del Guájaro</strong>
          <p>El embalse impulsa la pesca artesanal y crea identidad en torno al agua.</p>
        </div>
        <div class="item">
          <strong>Siglo XX</strong>
          <p>Crece la vida comunitaria: educación, deporte y cultura popular fortalecen el tejido social.</p>
        </div>
        <div class="item">
          <strong>Actualidad</strong>
          <p>La comunidad resalta la <em>unidad</em>, la <em>educación</em> y el carácter <em>jocoso</em> del pueblo.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="cultura" style="background:white">
    <div class="contenedor">
      <h2 class="titulo">Cultura y símbolos</h2>
      <p class="sub">Nuestros colores, tradiciones y alegría caribeña.</p>
      <div class="grid grid-3">
        <article class="card">
          <img src="https://images.unsplash.com/photo-1533636721434-0e2d61030955?q=80&w=1200&auto=format&fit=crop" alt="Tricolor azul, blanco y rojo en un diseño abstracto"/>
          <div class="card__caja">
            <h3>Colores Oficiales</h3>
            <p>Azul celeste, blanco y rojo. Reflejan el agua, la paz y la pasión de la comunidad.</p>
          </div>
        </article>
        <article class="card">
          <img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?q=80&w=1200&auto=format&fit=crop" alt="Árbol representativo"/>
          <div class="card__caja">
            <h3>Árbol de Pivijay</h3>
            <p>Símbolo natural de nuestra identidad. Representa vida, sombra y encuentro.</p>
          </div>
        </article>
        <article class="card">
          <img src="https://images.unsplash.com/photo-1508187589046-8f0f9f3f07fb?q=80&w=1200&auto=format&fit=crop" alt="Río y canoa artesanal"/>
          <div class="card__caja">
            <h3>Tradición Pesquera</h3>
            <p>La pesca artesanal y el río han marcado el carácter trabajador y solidario del pueblo.</p>
          </div>
        </article>
      </div>
    </div>
  </section>

  <section id="turismo">
    <div class="contenedor">
      <h2 class="titulo">Turismo y naturaleza</h2>
      <p class="sub">Rutas junto al agua, sabores locales y paisajes para descansar.</p>
      <div class="grid grid-2">
        <article class="card">
          <div class="card__caja">
            <h3>Paseos y experiencias</h3>
            <ul>
              <li>Recorridos por el <strong>Embalse del Guájaro</strong>.</li>
              <li>Observación de aves y atardeceres a la orilla.</li>
              <li>Gastronomía: pescado frito, yuca, bollo limpio.</li>
            </ul>
            <p style="margin-top:10px;color:#475569">Próximamente: agenda de festividades y fechas especiales.</p>
          </div>
        </article>
        <article class="card">
          <div class="card__caja">
            <h3>Cómo llegar</h3>
            <p>Estamos en jurisdicción de Sabanalarga (Atlántico). Actualiza aquí rutas y transporte.</p>
            <div style="margin-top:12px;border-radius:14px;overflow:hidden">
              <iframe title="Mapa de Aguada de Pablo" src="https://www.google.com/maps?q=Aguada%20de%20Pablo%2C%20Sabanalarga%2C%20Atl%C3%A1ntico&output=embed" width="100%" height="280" style="border:0"></iframe>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>

  <section id="directorio" style="background:white">
    <div class="contenedor">
      <h2 class="titulo">Directorio local</h2>
      <p class="sub">Espacio para promover negocios y servicios del corregimiento.</p>
      <div class="grid grid-3">
        <article class="card">
          <div class="card__caja">
            <h3>Restaurantes</h3>
            <p><strong>El Sazón del Guájaro</strong><br><small>Pescado fresco, platos típicos.</small></p>
            <p><strong>Doña Anita</strong><br><small>Bollo limpio y arepas.</small></p>
          </div>
        </article>
        <article class="card">
          <div class="card__caja">
            <h3>Alojamiento</h3>
            <p><strong>Cabañas del Embalse</strong><br><small>Vista al agua, ambiente familiar.</small></p>
            <p><strong>Hostal La Orilla</strong><br><small>Económico y cómodo.</small></p>
          </div>
        </article>
        <article class="card">
          <div class="card__caja">
            <h3>Otros servicios</h3>
            <p><strong>Artesanías La Rivera</strong><br><small>Tejidos y recuerdos locales.</small></p>
            <p><strong>Guías Comunitarios</strong><br><small>Recorridos por el embalse y río.</small></p>
          </div>
        </article>
      </div>
      <p style="margin-top:10px;color:#475569">*Ejemplos de demostración. Reemplaza con datos reales y teléfonos.</p>
    </div>
  </section>

  <section id="contacto">
    <div class="contenedor">
      <h2 class="titulo">Contacto comunitario</h2>
      <p class="sub">¿Quieres sumar tu negocio, enviar un evento o aportar fotos históricas? Escríbenos.</p>
      <div class="grid grid-2">
        <form class="card" onsubmit="enviar(event)">
          <div class="card__caja">
            <label>Nombre<br>
              <input required type="text" name="nombre" placeholder="Tu nombre" style="width:100%;padding:12px;border-radius:12px;border:1px solid #e5e7eb;margin-top:6px">
            </label>
            <div style="height:10px"></div>
            <label>Correo<br>
              <input required type="email" name="correo" placeholder="tunombre@email.com" style="width:100%;padding:12px;border-radius:12px;border:1px solid #e5e7eb;margin-top:6px">
            </label>
            <div style="height:10px"></div>
            <label>Mensaje<br>
              <textarea required name="mensaje" placeholder="Escribe tu mensaje" rows="5" style="width:100%;padding:12px;border-radius:12px;border:1px solid #e5e7eb;margin-top:6px"></textarea>
            </label>
            <div style="height:14px"></div>
            <button class="cta" style="border:none;cursor:pointer">Enviar</button>
          </div>
        </form>
        <aside>
          <div class="card">
            <div class="card__caja">
              <h3>Redes y enlaces</h3>
              <ul>
                <li><a href="#">Facebook de la comunidad</a></li>
                <li><a href="#">Instagram de turismo</a></li>
                <li><a href="#">WhatsApp del Comité</a></li>
              </ul>
              <p style="color:#475569">Agrega aquí los enlaces oficiales cuando estén disponibles.</p>
            </div>
          </div>
          <div style="height:20px"></div>
          <div class="card">
            <div class="card__caja">
              <h3>Descargas</h3>
              <ul>
                <li><a href="#">Guía del visitante (PDF)</a></li>
                <li><a href="#">Reglamento de uso del embalse</a></li>
                <li><a href="#">Escudo en alta calidad (SVG)</a></li>
              </ul>
              <p style="color:#475569">Súbelos a tu hosting y actualiza los enlaces.</p>
            </div>
          </div>
        </aside>
      </div>
    </div>
  </section>

  <footer>
    <div class="contenedor footer-grid">
      <div>
        <div class="footbrand">
          <div class="marca__escudo" aria-hidden="true" style="outline:3px solid var(--dorado)"></div>
          <div>
            <strong style="color:white;font-size:18px">Aguada de Pablo</strong>
            <div style="font-size:13px;color:#a6b2c5">Corregimiento de Sabanalarga · Atlántico</div>
          </div>
        </div>
        <p style="margin-top:10px;color:#9ca3af">Proyecto comunitario sin ánimo de lucro. Hecho con cariño por y para los aguadapablenses.</p>
      </div>
      <div>
        <div class="pill">Enlaces rápidos</div>
        <ul>
          <li><a href="#historia">Historia</a></li>
          <li><a href="#cultura">Cultura</a></li>
          <li><a href="#turismo">Turismo</a></li>
          <li><a href="#directorio">Directorio</a></li>
        </ul>
      </div>
      <div>
        <div class="pill" style="background:var(--azul)">Contacto</div>
        <p style="margin:.5rem 0 0">Correo: <a href="mailto:contacto@aguadadepablo.co">contacto@aguadadepablo.co</a></p>
        <p>Tel: <a href="tel:+573000000000">+57 300 000 0000</a></p>
      </div>
    </div>
    <div class="contenedor" style="margin-top:12px;font-size:12px;color:#94a3b8">
      © <span id="year"></span> Comunidad de Aguada de Pablo. Todos los derechos reservados.
    </div>
  </footer>

  <button class="float" onclick="scrollTo({top:0,behavior:'smooth'})" aria-label="Volver arriba">▲</button>

  <script>
    // Año dinámico en el footer
    document.getElementById('year').textContent = new Date().getFullYear();

    // Simulación de envío del formulario
    function enviar(e){
      e.preventDefault();
      const data = Object.fromEntries(new FormData(e.target).entries());
      alert(`¡Gracias, ${data.nombre}! Tu mensaje fue enviado.`);
      e.target.reset();
    }

    // Resaltar la sección activa mientras se hace scroll
    const links = document.querySelectorAll('nav a[href^="#"]');
    const secciones = [...links].map(a => document.querySelector(a.getAttribute('href')));
    const obs = new IntersectionObserver((entries)=>{
      entries.forEach(entry=>{
        const id = '#' + entry.target.id;
        const link = document.querySelector(`nav a[href="${id}"]`);
        if(entry.isIntersecting){
          links.forEach(a=>a.style.background='');
          if(link) link.style.background = 'rgba(30,144,255,.12)';
        }
      })
    },{threshold:.4});
    secciones.forEach(sec=>sec && obs.observe(sec));
  </script>
</body>
</html>
