<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Mi Página</title>
<style>
  :root{
    --bg:#111;
    --chrome:#1f1f1f;
    --chrome-2:#2a2a2a;
    --text:#e6e6e6;
    --muted:#a5a5a5;
    --accent:#3aa0ff;
    --card:#181818;
    --thumb:#0f0f0f;
    --radius:12px;
  }
  *{box-sizing:border-box}
  body{
    margin:0; background:linear-gradient(180deg,#0c0c0c,#171717);
    color:var(--text); font-family:system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,sans-serif;
    display:flex; align-items:center; justify-content:center; padding:24px;
  }
  .window{
    width:min(1000px,95vw);
    background:var(--bg); border-radius:18px; box-shadow:0 14px 40px rgba(0,0,0,.45);
    overflow:hidden; border:1px solid #2b2b2b;
  }
  /* fake browser chrome */
  .chrome{
    background:var(--chrome); padding:10px 14px; display:flex; align-items:center; gap:12px;
    border-bottom:1px solid #2b2b2b;
  }
  .dots{display:flex; gap:8px}
  .dot{width:12px; height:12px; border-radius:50%}
  .dot.red{background:#ff5f57} .dot.yellow{background:#febc2e} .dot.green{background:#28c840}
  .tab{background:var(--chrome-2); color:var(--text); padding:6px 12px; border-radius:10px}
  .addr{
    flex:1; background:#101010; border:1px solid #333; color:#cfcfcf; border-radius:999px;
    padding:8px 12px; overflow:hidden; white-space:nowrap; text-overflow:ellipsis;
  }
  .addr span{color:#9ad0ff}
  /* content area */
  .content{display:grid; grid-template-columns:2.3fr 1fr; gap:16px; padding:16px}
  .player{
    background:var(--card); border-radius:var(--radius); border:1px solid #282828; overflow:hidden;
  }
  .meta{padding:10px 4px; display:flex; align-items:center; gap:10px; color:var(--muted)}
  .meta .chip{color:#7aa7ff}
  .title{padding:0 4px 8px 4px; font-weight:600}
  /* sidebar */
  .side{display:flex; flex-direction:column; gap:10px}
  .suggest{
    display:grid; grid-template-columns:168px 1fr; gap:8px; background:var(--card);
    border:1px solid #272727; border-radius:10px; overflow:hidden;
  }
  .thumb{background:var(--thumb); aspect-ratio:16/9}
  .s-meta{padding:8px; font-size:.92rem}
  .s-title{font-weight:600}
  .s-chan,.s-views{color:var(--muted); font-size:.85rem}
  /* small */
  @media (max-width:900px){
    .content{grid-template-columns:1fr}
  }
</style>
</head>
<body>
  <div class="window">
    <div class="chrome">
      <div class="dots"><div class="dot red"></div><div class="dot yellow"></div><div class="dot green"></div></div>
      <div class="tab">Mi Página</div>
      <div class="addr">https://<span>mipagina.com</span>/index.html</div>
    </div>

    <div class="content">
      <!-- Player -->
      <div>
        <div class="player">
          <!-- Reemplaza el ID del video si quieres otro -->
          <iframe width="100%" height="480" src="https://www.youtube.com/embed/8hYlB38asDY"
                  title="Iron Man (2008) Trailer" frameborder="0"
                  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                  allowfullscreen></iframe>
        </div>
        <div class="meta">
          <span class="chip">#IRONMAN #MARVEL</span>
        </div>
        <div class="title">IRON MAN (2008) — Tráiler Oficial</div>
        <div class="meta" style="gap:18px">
          <span>35,620,861 visualizaciones • 5 oct. 2018</span>
          <span>👍 681k</span><span>💬 9802</span><span>⤴ Compartir</span><span>💾 Guardar</span>
        </div>
      </div>

      <!-- Sidebar -->
      <aside class="side">
        <div class="suggest">
          <div class="thumb"></div>
          <div class="s-meta">
            <div class="s-title">IRON MAN 2 — Tráiler</div>
            <div class="s-chan">Marvel Entertainment</div>
            <div class="s-views">133 M visualizaciones • hace 1 año</div>
          </div>
        </div>
        <div class="suggest">
          <div class="thumb"></div>
          <div class="s-meta">
            <div class="s-title">La primera armadura de Tony</div>
            <div class="s-chan">Clips Marvel</div>
            <div class="s-views">50+ • YouTube</div>
          </div>
        </div>
        <div class="suggest">
          <div class="thumb"></div>
          <div class="s-meta">
            <div class="s-title">IRON MAN 3 — Tráiler</div>
            <div class="s-chan">Marvel</div>
            <div class="s-views">46 M visualizaciones • 11 meses</div>
          </div>
        </div>
        <div class="suggest">
          <div class="thumb"></div>
          <div class="s-meta">
            <div class="s-title">Detrás de cámaras de IRON MAN</div>
            <div class="s-chan">Featurettes</div>
            <div class="s-views">6,1 M visualizaciones • hace 1 año</div>
          </div>
        </div>
      </aside>
    </div>
  </div>
</body>
</html>
