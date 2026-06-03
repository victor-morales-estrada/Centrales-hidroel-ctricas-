<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Energía Hidráulica — 1º Bach B</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;0,700;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
:root {
  --ink: #0e1a2b;
  --deep: #112240;
  --mid: #1a4a7a;
  --water: #1e88c8;
  --foam: #5ac8f5;
  --ice: #a8dff5;
  --sand: #f5f0e8;
  --gold: #c8a455;
  --gold-light: #e8c878;
  --white: #ffffff;
  --text: #1a2535;
  --muted: #5a7090;
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{
  font-family:'DM Sans',sans-serif;
  background:var(--sand);
  color:var(--text);
  font-size:15px;
  line-height:1.75;
}

/* ===== PORTADA ===== */
.cover{
  min-height:100vh;
  background:var(--ink);
  display:flex;
  flex-direction:column;
  justify-content:space-between;
  padding:0;
  position:relative;
  overflow:hidden;
}
.cover-bg{
  position:absolute;inset:0;
  background:
    radial-gradient(ellipse 70% 50% at 30% 20%, rgba(30,136,200,0.22) 0%,transparent 55%),
    radial-gradient(ellipse 50% 60% at 80% 80%, rgba(90,200,245,0.1) 0%,transparent 50%),
    radial-gradient(ellipse 40% 30% at 60% 10%, rgba(200,164,85,0.08) 0%,transparent 40%);
  pointer-events:none;
}
.cover-wave{
  position:absolute;bottom:0;left:0;right:0;
}
.cover-top{
  padding:48px 64px 0;
  display:flex;
  justify-content:space-between;
  align-items:flex-start;
  position:relative;z-index:2;
}
.cover-badge{
  font-size:0.68rem;
  letter-spacing:0.25em;
  text-transform:uppercase;
  color:var(--foam);
  opacity:0.8;
}
.cover-members{
  text-align:right;
}
.cover-members p{
  font-size:0.72rem;
  color:rgba(255,255,255,0.45);
  line-height:1.9;
  letter-spacing:0.03em;
}
.cover-members p strong{
  color:rgba(255,255,255,0.75);
  font-weight:500;
}
.cover-center{
  flex:1;
  display:flex;
  flex-direction:column;
  justify-content:center;
  padding:60px 64px;
  position:relative;z-index:2;
}
.cover-eyebrow{
  font-size:0.7rem;
  letter-spacing:0.3em;
  text-transform:uppercase;
  color:var(--gold);
  margin-bottom:18px;
}
.cover-h1{
  font-family:'Cormorant Garamond',serif;
  font-size:clamp(3rem,7vw,6.5rem);
  font-weight:700;
  color:var(--white);
  line-height:1.0;
  margin-bottom:12px;
}
.cover-h1 em{
  font-style:italic;
  color:var(--foam);
}
.cover-subtitle{
  font-size:1rem;
  color:rgba(255,255,255,0.5);
  max-width:480px;
  font-weight:300;
  margin-bottom:40px;
  line-height:1.6;
}
.cover-line{
  width:60px;height:2px;
  background:linear-gradient(90deg,var(--gold),var(--foam));
  margin-bottom:28px;
}
.cover-meta{
  display:flex;gap:32px;flex-wrap:wrap;
}
.cover-meta-item{
  display:flex;flex-direction:column;gap:3px;
}
.cover-meta-item span:first-child{
  font-size:0.62rem;letter-spacing:0.2em;text-transform:uppercase;color:var(--gold);opacity:0.7;
}
.cover-meta-item span:last-child{
  font-size:0.82rem;color:rgba(255,255,255,0.7);
}

/* ===== NAVIGATION INDEX ===== */
.nav-section{
  background:var(--deep);
  padding:48px 64px;
}
.nav-title{
  font-family:'Cormorant Garamond',serif;
  font-size:0.75rem;
  letter-spacing:0.3em;
  text-transform:uppercase;
  color:var(--foam);
  margin-bottom:28px;
}
.nav-grid{
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(220px,1fr));
  gap:8px;
}
.nav-item{
  display:flex;align-items:center;gap:14px;
  padding:12px 16px;
  border:1px solid rgba(90,200,245,0.12);
  border-radius:4px;
  text-decoration:none;
  color:rgba(255,255,255,0.6);
  font-size:0.82rem;
  transition:all 0.2s;
  cursor:pointer;
}
.nav-item:hover{border-color:var(--foam);color:var(--white);background:rgba(90,200,245,0.07);}
.nav-n{
  font-family:'Cormorant Garamond',serif;
  font-size:1.4rem;color:var(--foam);opacity:0.5;min-width:22px;line-height:1;
}

/* ===== MAIN LAYOUT ===== */
.wrap{max-width:960px;margin:0 auto;padding:0 48px 80px;}

/* ===== SECTIONS ===== */
.section{padding:64px 0 0;}
.section-header{
  display:flex;align-items:flex-start;gap:20px;
  padding-bottom:20px;
  border-bottom:1px solid rgba(0,0,0,0.08);
  margin-bottom:28px;
}
.section-n{
  font-family:'Cormorant Garamond',serif;
  font-size:4.5rem;font-weight:700;
  color:var(--water);opacity:0.12;
  line-height:1;min-width:56px;margin-top:-10px;
}
.section-head-text .label{
  font-size:0.65rem;letter-spacing:0.25em;text-transform:uppercase;
  color:var(--water);margin-bottom:4px;
}
.section-head-text h2{
  font-family:'Cormorant Garamond',serif;
  font-size:clamp(1.6rem,3vw,2.3rem);font-weight:700;
  color:var(--ink);line-height:1.1;
}
.body-text{
  font-size:0.93rem;line-height:1.85;color:#2a3545;
  margin-bottom:16px;
}
.body-text strong{color:var(--ink);font-weight:500;}

/* ===== CALLOUT ===== */
.callout{
  background:var(--deep);
  border-left:3px solid var(--foam);
  padding:18px 24px;
  margin:24px 0;
  border-radius:0 4px 4px 0;
}
.callout p{font-size:0.88rem;line-height:1.7;color:rgba(255,255,255,0.8);}
.callout .icon{font-size:1.2rem;display:block;margin-bottom:6px;}

/* ===== TABLE ===== */
.data-table{width:100%;border-collapse:collapse;margin:20px 0;font-size:0.85rem;}
.data-table th{
  background:var(--deep);color:var(--foam);
  padding:10px 14px;text-align:left;font-weight:500;letter-spacing:0.04em;
}
.data-table td{padding:9px 14px;border-bottom:1px solid rgba(0,0,0,0.06);}
.data-table tr:nth-child(even) td{background:rgba(30,136,200,0.04);}
.data-table tr:hover td{background:rgba(90,200,245,0.08);}

/* ===== GRID CARDS ===== */
.cards{display:grid;grid-template-columns:1fr 1fr;gap:16px;margin:20px 0;}
.card{
  background:var(--deep);border:1px solid rgba(90,200,245,0.12);
  border-radius:4px;padding:20px;
}
.card h4{font-family:'Cormorant Garamond',serif;color:var(--foam);font-size:1rem;margin-bottom:8px;}
.card p{font-size:0.82rem;line-height:1.7;color:rgba(255,255,255,0.7);}

/* ===== LIST ===== */
.tech-list{list-style:none;margin:16px 0;}
.tech-list li{
  padding:9px 0 9px 24px;
  border-bottom:1px solid rgba(0,0,0,0.05);
  position:relative;font-size:0.88rem;
}
.tech-list li::before{content:'▸';position:absolute;left:0;color:var(--foam);font-size:0.75rem;top:11px;}

/* ===== IMG BLOCK ===== */
.fig{margin:24px 0;border-radius:6px;overflow:hidden;border:1px solid rgba(0,0,0,0.08);}
.fig-cap{
  background:var(--deep);color:rgba(255,255,255,0.5);
  font-size:0.72rem;padding:7px 14px;font-style:italic;letter-spacing:0.02em;
}

/* ===== DIVIDER ===== */
.div{height:1px;background:linear-gradient(90deg,transparent,rgba(30,136,200,0.25),transparent);margin:56px 0 0;}

/* ===== BADGE ===== */
.badge{
  display:inline-block;background:rgba(30,136,200,0.1);
  border:1px solid rgba(30,136,200,0.25);color:var(--mid);
  font-size:0.7rem;padding:3px 9px;border-radius:2px;
  margin:3px;letter-spacing:0.04em;
}

/* ===== FORMULA BOX ===== */
.formula{
  background:var(--ink);color:var(--ice);
  font-family:'Cormorant Garamond',serif;font-size:1.3rem;
  text-align:center;padding:20px;border-radius:4px;
  border:1px solid rgba(90,200,245,0.2);margin:20px 0;
  letter-spacing:0.06em;
}
.formula small{font-size:0.7rem;color:rgba(255,255,255,0.4);display:block;margin-top:6px;font-family:'DM Sans',sans-serif;letter-spacing:0.05em;}

/* ===== STAT BOXES ===== */
.stats{display:flex;gap:12px;flex-wrap:wrap;margin:20px 0;}
.stat{
  flex:1;min-width:120px;
  background:var(--ink);border:1px solid rgba(90,200,245,0.15);
  border-radius:4px;padding:16px;text-align:center;
}
.stat-val{
  font-family:'Cormorant Garamond',serif;
  font-size:2rem;font-weight:700;color:var(--foam);line-height:1;
  margin-bottom:4px;
}
.stat-label{font-size:0.7rem;color:rgba(255,255,255,0.4);letter-spacing:0.08em;text-transform:uppercase;}

/* ===== TURBINE TYPE CARDS ===== */
.turb-cards{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin:20px 0;}
.turb-card{
  background:var(--ink);border:1px solid rgba(90,200,245,0.15);
  border-radius:6px;overflow:hidden;
}
.turb-head{background:rgba(30,136,200,0.15);padding:14px;text-align:center;}
.turb-head h4{font-family:'Cormorant Garamond',serif;color:var(--foam);font-size:1.15rem;}
.turb-head .range{font-size:0.72rem;color:var(--gold);margin-top:2px;}
.turb-body{padding:14px;}
.turb-body p{font-size:0.78rem;color:rgba(255,255,255,0.6);line-height:1.6;}

/* ===== FLOW DIAGRAM ===== */
.flow{display:flex;align-items:center;gap:6px;margin:20px 0;flex-wrap:wrap;}
.flow-step{
  background:var(--deep);border:1px solid rgba(90,200,245,0.2);
  border-radius:4px;padding:10px 14px;text-align:center;flex:1;min-width:80px;
}
.flow-step .fs-n{font-size:0.6rem;color:var(--gold);letter-spacing:0.15em;text-transform:uppercase;}
.flow-step .fs-t{font-size:0.78rem;color:var(--white);font-weight:500;margin-top:2px;}
.flow-step .fs-e{font-size:0.65rem;color:var(--foam);margin-top:1px;}
.flow-arr{color:var(--water);font-size:1rem;opacity:0.6;flex-shrink:0;}

/* ===== REGION BOXES ===== */
.region-box{
  background:linear-gradient(135deg,var(--deep),var(--ink));
  border:1px solid rgba(200,164,85,0.2);border-radius:6px;
  padding:20px 24px;margin:16px 0;
}
.region-box h4{font-family:'Cormorant Garamond',serif;color:var(--gold);font-size:1.1rem;margin-bottom:8px;}
.region-box p{font-size:0.85rem;color:rgba(255,255,255,0.65);line-height:1.7;}

/* ===== CONCLUSION ===== */
.conclusion{
  background:var(--deep);
  padding:48px;
  border-radius:8px;
  margin:40px 0;
  border:1px solid rgba(90,200,245,0.12);
  position:relative;overflow:hidden;
}
.conclusion::before{
  content:'';position:absolute;top:0;left:0;right:0;height:3px;
  background:linear-gradient(90deg,var(--gold),var(--foam),var(--water));
}
.conclusion h2{
  font-family:'Cormorant Garamond',serif;
  font-size:1.8rem;color:var(--white);margin-bottom:16px;
}
.conclusion p{font-size:0.9rem;color:rgba(255,255,255,0.7);line-height:1.85;margin-bottom:12px;}
  <!-- TURBINAS -->
  <div class="turb-cards">
    <div class="turb-card">
      <div class="turb-head">
        <h4>Turbina Pelton</h4>
        <div class="range">Salto &gt; 200 m · Caudal pequeño</div>
      </div>
      <div class="turb-body">
        <p>Turbina de <strong>acción</strong>. El agua sale por inyectores en forma de chorro a gran velocidad que impacta en cazos (cucharas) del rodete. Eje horizontal o vertical. Alta montaña.</p>
      </div>
    </div>
    <div class="turb-card">
      <div class="turb-head">
        <h4>Turbina Francis</h4>
        <div class="range">Salto 20–200 m · Caudal moderado</div>
      </div>
      <div class="turb-body">
        <p>Turbina de <strong>reacción</strong> mixta. El agua entra en espiral por la carcasa, atraviesa el distribuidor de paletas y el rodete. La más utilizada en el mundo. Eje vertical.</p>
      </div>
    </div>
    <div class="turb-card">
      <div class="turb-head">
        <h4>Turbina Kaplan</h4>
        <div class="range">Salto &lt; 20 m · Gran caudal</div>
      </div>
      <div class="turb-body">
        <p>Turbina de <strong>reacción axial</strong>. Paletas ajustables que permiten adaptarse al caudal. Ideal para grandes ríos de llanura con pequeños desniveles. Alta eficiencia en rango amplio.</p>
      </div>
    </div>
  </div>

  <div class="fig">
    <svg viewBox="0 0 700 180" width="100%" fill="none" xmlns="http://www.w3.org/2000/svg">
      <rect width="700" height="180" fill="#0e1a2b"/>
      <text x="350" y="16" fill="#5ac8f5" font-size="9" text-anchor="middle" font-family="serif" letter-spacing="0.5">ESQUEMA SIMPLIFICADO DE TURBINAS</text>
      <!-- PELTON -->
      <g transform="translate(20,25)"><rect width="210" height="130" fill="#112240" rx="3"/>
        <circle cx="105" cy="68" r="48" fill="none" stroke="#5ac8f5" stroke-width="1" opacity="0.25"/>
        <circle cx="105" cy="68" r="3" fill="#5ac8f5" opacity="0.7"/>
        <g opacity="0.7" fill="#0d2a50" stroke="#5ac8f5" stroke-width="1">
          <path d="M105,20 Q118,28 120,42 Q122,56 110,62 Q98,68 88,62 Q78,56 82,42 Q86,28 105,20Z"/>
          <path d="M145,34 Q156,46 152,60 Q148,74 136,74 Q124,74 120,62 Q116,50 124,42 Q132,34 145,34Z"/>
          <path d="M155,76 Q160,91 152,102 Q144,113 132,110 Q120,107 118,94 Q116,81 126,75 Q136,69 155,76Z"/>
          <path d="M130,112 Q133,128 122,135 Q111,142 102,136 Q93,130 96,118 Q99,106 110,104Z"/>
          <path d="M90,118 Q88,134 76,138 Q64,142 57,134 Q50,126 56,115 Q62,104 74,105Z"/>
          <path d="M56,100 Q47,113 36,110 Q25,107 24,95 Q23,83 33,78 Q43,73 52,81Z"/>
          <path d="M48,62 Q40,75 28,70 Q16,65 16,53 Q16,41 28,39 Q40,37 46,48Z"/>
          <path d="M63,30 Q57,44 46,40 Q35,36 36,24 Q37,12 49,11 Q61,10 65,22Z"/>
        </g>
        <path d="M-5,66 Q18,66 32,68" stroke="#00e5ff" stroke-width="4" stroke-linecap="round" opacity="0.7"/>
        <text x="105" y="152" fill="#5ac8f5" font-size="9" text-anchor="middle" font-family="serif" font-weight="bold">PELTON</text>
        <text x="105" y="163" fill="rgba(255,255,255,0.35)" font-size="7" text-anchor="middle">chorro a presión → cazos</text>
      </g>
      <!-- FRANCIS -->
      <g transform="translate(245,25)"><rect width="210" height="130" fill="#112240" rx="3"/>
        <path d="M105,68 m-55,0 a55,55 0 1,1 110,0 a55,55 0 0,1 -75,42 Q48,118 48,98" fill="none" stroke="#5ac8f5" stroke-width="7" opacity="0.25"/>
        <circle cx="105" cy="68" r="36" fill="none" stroke="#1e88c8" stroke-width="5" opacity="0.4"/>
        <circle cx="105" cy="68" r="22" fill="#0d2a50" opacity="0.85" stroke="#5ac8f5" stroke-width="1.2"/>
        <g fill="none" stroke="#5ac8f5" stroke-width="1.2" opacity="0.8">
          <path d="M105,46 Q120,52 122,66 Q124,80 112,87 Q100,94 90,88 Q80,82 82,68 Q84,54 95,48"/>
          <path d="M122,66 Q130,54 125,69 M105,90 Q95,97 105,82"/>
        </g>
        <line x1="105" y1="46" x2="105" y2="18" stroke="#c8a455" stroke-width="2" opacity="0.6"/>
        <path d="M105,90 Q105,108 105,120" stroke="#1e88c8" stroke-width="10" opacity="0.5"/>
        <path d="M30,68 Q55,68 68,68" stroke="#00e5ff" stroke-width="4" stroke-linecap="round" opacity="0.6"/>
        <text x="105" y="152" fill="#5ac8f5" font-size="9" text-anchor="middle" font-family="serif" font-weight="bold">FRANCIS</text>
        <text x="105" y="163" fill="rgba(255,255,255,0.35)" font-size="7" text-anchor="middle">espiral → rodete → tubo asp.</text>
      </g>
      <!-- KAPLAN -->
      <g transform="translate(470,25)"><rect width="210" height="130" fill="#112240" rx="3"/>
        <rect x="30" y="58" width="150" height="22" fill="#0d2a50" opacity="0.7" rx="3"/>
        <rect x="30" y="60" width="150" height="18" fill="#1a4a7a" opacity="0.5" rx="2"/>
        <circle cx="105" cy="68" r="18" fill="#0d2a50" opacity="0.85" stroke="#5ac8f5" stroke-width="1.5"/>
        <g fill="none" stroke="#5ac8f5" stroke-width="2" opacity="0.8">
          <path d="M105,50 Q116,56 117,68 Q118,80 105,86" />
          <path d="M105,50 Q116,56 117,68 Q118,80 105,86" transform="rotate(72,105,68)"/>
          <path d="M105,50 Q116,56 117,68 Q118,80 105,86" transform="rotate(144,105,68)"/>
          <path d="M105,50 Q116,56 117,68 Q118,80 105,86" transform="rotate(216,105,68)"/>
          <path d="M105,50 Q116,56 117,68 Q118,80 105,86" transform="rotate(288,105,68)"/>
        </g>
        <circle cx="105" cy="68" r="4.5" fill="#5ac8f5" opacity="0.7"/>
        <path d="M20,67 L38,67" stroke="#00e5ff" stroke-width="1.5" marker-end="url(#aF)" opacity="0.7"/>
        <path d="M172,67 L190,67" stroke="#00e5ff" stroke-width="1.5" marker-end="url(#aF)" opacity="0.7"/>
        <line x1="105" y1="50" x2="105" y2="22" stroke="#c8a455" stroke-width="2" opacity="0.6"/>
        <text x="105" y="152" fill="#5ac8f5" font-size="9" text-anchor="middle" font-family="serif" font-weight="bold">KAPLAN</text>
        <text x="105" y="163" fill="rgba(255,255,255,0.35)" font-size="7" text-anchor="middle">flujo axial · paletas ajustables</text>
      </g>
    </svg>
    <div class="fig-cap">Fig. 4 — Esquemas de los tres tipos de turbinas hidráulicas: Pelton (acción), Francis y Kaplan (reacción)</div>
  </div>

  <!-- 7. CANAL DESAGÜE -->
  <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.4rem;color:var(--ink);margin:32px 0 10px;padding-left:16px;border-left:3px solid var(--foam);">⑦ Canal de Desagüe</h3>
  <p class="body-text">Conducción que <strong>restituye el agua al cauce natural</strong> una vez extraída su energía. Su cota determina el nivel de descarga inferior del salto bruto. Debe incluir <em>escala de peces</em> (obligatoria legalmente para garantizar la continuidad ecológica del río) y respetar el <strong>caudal ecológico mínimo</strong> legalmente establecido.</p>

  <!-- 8. PARQUE TRANSFORMACIONES -->
  <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.4rem;color:var(--ink);margin:32px 0 10px;padding-left:16px;border-left:3px solid var(--foam);">⑧ Parque de Transformaciones</h3>
  <p class="body-text">Subestación elevadora que sube la tensión de los alternadores (<strong>6–20 kV</strong>) a la tensión de transporte (<strong>66–400 kV</strong>) para reducir pérdidas en la línea. Contiene transformadores elevadores, interruptores de potencia, seccionadores, pararrayos y transformadores de medida (TT/TI).</p>

  <div class="fig">
    <svg viewBox="0 0 700 120" width="100%" fill="none" xmlns="http://www.w3.org/2000/svg">
      <rect width="700" height="120" fill="#0e1a2b"/>
      <text x="350" y="15" fill="#c8a455" font-size="9" text-anchor="middle" font-family="serif" letter-spacing="0.5">DIAGRAMA UNIFILAR — EVACUACIÓN ELÉCTRICA</text>
      <defs><marker id="aE" markerWidth="5" markerHeight="5" refX="2.5" refY="2.5" orient="auto"><path d="M0,0 L0,5 L5,2.5z" fill="#c8a455"/></marker></defs>
      <!-- Alternador -->
      <circle cx="55" cy="72" r="24" fill="#112240" stroke="#5ac8f5" stroke-width="1.3"/>
      <text x="55" y="68" fill="#5ac8f5" font-size="8" text-anchor="middle" font-family="serif">ALT</text>
      <text x="55" y="78" fill="#5ac8f5" font-size="9" text-anchor="middle">~</text>
      <text x="55" y="105" fill="rgba(255,255,255,0.4)" font-size="7" text-anchor="middle">6-20 kV</text>
      <!-- cable BT -->
      <line x1="79" y1="72" x2="110" y2="72" stroke="#5ac8f5" stroke-width="2.5" opacity="0.7"/>
      <!-- Int. salida -->
      <rect x="110" y="63" width="16" height="18" fill="#112240" stroke="#5ac8f5" stroke-width="1" rx="2"/>
      <text x="118" y="92" fill="rgba(255,255,255,0.35)" font-size="6.5" text-anchor="middle">Int.</text>
      <line x1="118" y1="63" x2="118" y2="55" stroke="#5ac8f5" stroke-width="1.3"/>
      <line x1="118" y1="81" x2="118" y2="89" stroke="#5ac8f5" stroke-width="1.3"/>
      <line x1="118" y1="89" x2="158" y2="89" stroke="#5ac8f5" stroke-width="2" opacity="0.6"/>
      <!-- Transformador -->
      <g transform="translate(158,42)">
        <rect x="0" y="0" width="52" height="60" rx="2" fill="#1a1628" stroke="#c8a455" stroke-width="1.3"/>
        <circle cx="26" cy="20" r="13" fill="none" stroke="#c8a455" stroke-width="1.2"/>
        <circle cx="26" cy="40" r="13" fill="none" stroke="#c8a455" stroke-width="1.2"/>
        <text x="26" y="75" fill="#c8a455" font-size="7.5" text-anchor="middle" font-family="serif">TRAFO</text>
      </g>
      <!-- cable AT -->
      <line x1="210" y1="72" x2="258" y2="72" stroke="#c8a455" stroke-width="2" opacity="0.7"/>
      <!-- Int AT -->
      <rect x="258" y="63" width="16" height="18" fill="#1a1628" stroke="#c8a455" stroke-width="1" rx="2"/>
      <line x1="266" y1="63" x2="266" y2="55" stroke="#c8a455" stroke-width="1.3"/>
      <line x1="266" y1="81" x2="266" y2="89" stroke="#c8a455" stroke-width="1.3"/>
      <!-- Barras AT -->
      <line x1="266" y1="89" x2="480" y2="89" stroke="#c8a455" stroke-width="3" opacity="0.65"/>
      <text x="370" y="100" fill="#c8a455" font-size="7.5" text-anchor="middle" font-family="serif">BARRAS AT (132 kV)</text>
      <!-- Pararrayo -->
      <line x1="340" y1="89" x2="340" y2="68" stroke="#c8a455" stroke-width="1.2"/>
      <path d="M334,75 L346,75 L340,84 L346,84 L334,92" stroke="#c8a455" stroke-width="1" fill="none"/>
      <text x="340" y="62" fill="rgba(255,255,255,0.3)" font-size="6.5" text-anchor="middle">Pararrayo</text>
      <!-- TT/TI -->
      <rect x="400" y="60" width="26" height="18" fill="#1a1628" stroke="#c8a455" stroke-width="1" rx="2"/>
      <text x="413" y="72" fill="#c8a455" font-size="7" text-anchor="middle">TT/TI</text>
      <!-- Secc. -->
      <line x1="450" y1="89" x2="480" y2="72" stroke="#c8a455" stroke-width="1.3" opacity="0.7"/>
      <!-- Línea transmisión -->
      <line x1="480" y1="72" x2="560" y2="72" stroke="#c8a455" stroke-width="1.5" stroke-dasharray="5,3" opacity="0.6"/>
      <!-- Torres -->
      <g stroke="#c8a455" stroke-width="1.3" opacity="0.7">
        <line x1="575" y1="35" x2="575" y2="85"/>
        <line x1="562" y1="50" x2="588" y2="50"/>
        <line x1="565" y1="58" x2="585" y2="58"/>
        <line x1="575" y1="50" x2="569" y2="62"/>
        <line x1="575" y1="50" x2="581" y2="62"/>
        <circle cx="562" cy="50" r="2.5" fill="#c8a455" opacity="0.5"/>
        <circle cx="588" cy="50" r="2.5" fill="#c8a455" opacity="0.5"/>
        <circle cx="565" cy="58" r="2" fill="#c8a455" opacity="0.4"/>
        <circle cx="585" cy="58" r="2" fill="#c8a455" opacity="0.4"/>
      </g>
      <line x1="588" y1="50" x2="640" y2="50" stroke="#c8a455" stroke-width="1" stroke-dasharray="4,3" opacity="0.5" marker-end="url(#aE)"/>
      <text x="660" y="54" fill="rgba(255,255,255,0.4)" font-size="7.5" font-family="serif">Red</text>
      <text x="184" y="36" fill="rgba(255,255,255,0.35)" font-size="7" text-anchor="middle">↑ 6 kV</text>
      <text x="230" y="36" fill="rgba(255,255,255,0.35)" font-size="7" text-anchor="middle">132 kV ↑</text>
    </svg>
    <div class="fig-cap">Fig. 5 — Diagrama unifilar simplificado: alternador → transformador elevador → barras AT → línea de alta tensión</div>
  </div>

  <table class="data-table">
    <tr><th>Elemento</th><th>Función principal</th><th>Dato técnico</th></tr>
    <tr><td>Presa</td><td>Crear el embalse y el salto hidráulico</td><td>Puede superar 300 m de altura</td></tr>
    <tr><td>Toma de agua</td><td>Captar y filtrar el caudal</td><td>Equipada con rejas y compuerta de guardia</td></tr>
    <tr><td>Canal derivación</td><td>Conducir agua a presión atmosférica</td><td>Pendiente 0,001–0,003 m/m · v = 1–3 m/s</td></tr>
    <tr><td>Cámara de presión</td><td>Regularizar el flujo y decantar sedimentos</td><td>Volumen: 5–10 min de suministro</td></tr>
    <tr><td>Tubería de presión</td><td>Conducir agua a alta presión hasta la turbina</td><td>Acero · hasta 150 bar en grandes saltos</td></tr>
    <tr><td>Cámara de turbinas</td><td>Conversión hidráulica → mecánica → eléctrica</td><td>Rendimiento global ~88–92%</td></tr>
    <tr><td>Canal desagüe</td><td>Restituir el agua al río</td><td>Caudal ecológico mínimo obligatorio</td></tr>
    <tr><td>Parque transformaciones</td><td>Elevar tensión para transporte en red</td><td>6–20 kV → 66–400 kV</td></tr>
  </table>
</section>

<div class="div"></div>

<!-- ====== IV. CLASIFICACIÓN ====== -->
<section class="section" id="clasificacion">
  <div class="section-header">
    <div class="section-n">IV</div>
    <div class="section-head-text">
      <p class="label">Tipologías y criterios</p>
      <h2>Clasificación de las Centrales Hidroeléctricas</h2>
    </div>
  </div>

  <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.2rem;color:var(--mid);margin:0 0 12px;">A · Según su concepción estructural</h3>
  <div class="cards">
    <div class="card"><h4>💧 Agua Fluyente</h4><p>Sin embalse significativo. Usan el caudal natural del río. La producción depende del régimen de lluvias. No regulables según demanda.</p></div>
    <div class="card"><h4>🏔️ Regulación (Embalse)</h4><p>Presa crea lago artificial para almacenar agua. Permiten generar según la demanda, independientemente del caudal del río.</p></div>
    <div class="card"><h4>⚡ Bombeo (Reversibles)</h4><p>Dos embalses a distinta cota. En horas punta: turbina. En horas valle: bomba. Actúan como <em>"batería gigante"</em> del sistema eléctrico.</p></div>
    <div class="card"><h4>🌊 Hidráulica de Mareas</h4><p>Aprovechan el ciclo de mareas en estuarios. Menos extendidas, pero con potencial en costas con grandes mareas (ej. La Rance, Francia).</p></div>
  </div>

  <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.2rem;color:var(--mid);margin:20px 0 12px;">B · Según la altura del salto</h3>
  <table class="data-table">
    <tr><th>Tipo</th><th>Salto (H)</th><th>Caudal</th><th>Turbina</th><th>Ejemplo</th></tr>
    <tr><td><strong>Alta presión</strong></td><td>&gt; 200 m</td><td>Pequeño</td><td>Pelton</td><td>Alta montaña alpina</td></tr>
    <tr><td><strong>Media presión</strong></td><td>20–200 m</td><td>Moderado</td><td>Francis</td><td>Valles y ríos medianos</td></tr>
    <tr><td><strong>Baja presión</strong></td><td>&lt; 20 m</td><td>Grande</td><td>Kaplan / Hélice</td><td>Grandes ríos de llanura</td></tr>
  </table>

  <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.2rem;color:var(--mid);margin:20px 0 12px;">C · Según la potencia instalada</h3>
  <div class="stats">
    <div class="stat"><div class="stat-val">&lt;1 MW</div><div class="stat-label">Microcentral</div></div>
    <div class="stat"><div class="stat-val">1–10 MW</div><div class="stat-label">Minicentral</div></div>
    <div class="stat"><div class="stat-val">&gt;10 MW</div><div class="stat-label">Gran central</div></div>
    <div class="stat"><div class="stat-val">22.500 MW</div><div class="stat-label">Tres Gargantas (China)</div></div>
  </div>
</section>

<div class="div"></div>

<!-- ====== V. EMPLAZAMIENTO ====== -->
<section class="section" id="emplazamiento">
  <div class="section-header">
    <div class="section-n">V</div>
    <div class="section-head-text">
      <p class="label">Localización y criterios técnicos</p>
      <h2>Emplazamiento de Sistemas Hidráulicos</h2>
    </div>
  </div>

  <p class="body-text">La elección del emplazamiento es decisiva para la viabilidad técnica y económica de una central. Los <strong>factores determinantes</strong> son:</p>

  <div class="cards">
    <div class="card"><h4>🌊 Disponibilidad hídrica</h4><p>Caudal suficiente y regular a lo largo del año, incluyendo períodos secos. Se analiza la serie histórica de aforos del río.</p></div>
    <div class="card"><h4>📐 Desnivel topográfico</h4><p>Mayor desnivel = mayor salto H = mayor potencia. Los valles en "V" de montaña son ideales para grandes saltos con embalse compacto.</p></div>
    <div class="card"><h4>🌿 Impacto ambiental</h4><p>Estudios de impacto ambiental (EIA) obligatorios. Se evalúa la afección a fauna, flora, hábitats y población.</p></div>
    <div class="card"><h4>🏙️ Proximidad a la demanda</h4><p>Menor distancia a centros de consumo reduce costes y pérdidas en el transporte eléctrico.</p></div>
    <div class="card"><h4>🪨 Geología y estabilidad</h4><p>El terreno debe ser impermeable y resistente para soportar la presa y el embalse sin filtraciones ni riesgos de deslizamiento.</p></div>
    <div class="card"><h4>🚧 Accesibilidad</h4><p>Posibilidad de construir vías de acceso para maquinaria pesada, materiales y posterior operación y mantenimiento.</p></div>
  </div>

  <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.2rem;color:var(--mid);margin:20px 0 12px;">Tipos de emplazamiento</h3>
  <ul class="tech-list">
    <li><strong>En ríos:</strong> zonas con caudal constante o semiestacional. Son los más comunes a nivel mundial.</li>
    <li><strong>En zonas montañosas:</strong> aprovechan grandes desniveles. Centrales de alta presión con túneles y largos canales de derivación.</li>
    <li><strong>En embalses existentes:</strong> se añade una central a una presa ya construida para abastecimiento o riego, maximizando el aprovechamiento del recurso.</li>
    <li><strong>En canales de riego:</strong> minicentrales que aprovechan el caudal circulante en infraestructuras agrícolas existentes con impacto ambiental mínimo.</li>
  </ul>
</section>

<div class="div"></div>

<!-- ====== VI. IMPACTO AMBIENTAL ====== -->
<section class="section" id="impacto">
  <div class="section-header">
    <div class="section-n">VI</div>
    <div class="section-head-text">
      <p class="label">Medio ambiente y sostenibilidad</p>
      <h2>Impacto Ambiental</h2>
    </div>
  </div>

  <p class="body-text">Aunque la energía hidroeléctrica es renovable y no emite CO₂ durante su operación, la construcción y el funcionamiento de presas y centrales pueden <strong>alterar significativamente los ecosistemas fluviales</strong>. Por ello, la legislación exige Estudios de Impacto Ambiental previos.</p>

  <div class="pros-cons">
    <div class="pros">
      <h4>Ventajas ambientales</h4>
      <ul>
        <li>Energía renovable sin emisiones directas</li>
        <li>Sin residuos radiactivos ni contaminantes</li>
        <li>Regulación de crecidas e inundaciones</li>
        <li>Almacenamiento hídrico para sequías</li>
        <li>Larga vida útil (50–100 años)</li>
      </ul>
    </div>
    <div class="cons">
      <h4>Impactos negativos</h4>
      <ul>
        <li>Inundación de territorios y ecosistemas</li>
        <li>Interrupción de la continuidad fluvial</li>
        <li>Bloqueo de la migración de peces</li>
        <li>Cambios en temperatura y calidad del agua</li>
        <li>Retención de sedimentos aguas arriba</li>
      </ul>
    </div>
  </div>

  <div class="callout">
    <span class="icon">🐟</span>
    <p><strong>Medidas correctoras:</strong> La ley obliga a instalar <em>escalas de peces</em>, respetar el <em>caudal ecológico mínimo</em> (normalmente 10% del caudal medio), construir <em>pasos para fauna terrestre</em> y realizar seguimiento ambiental continuo durante la explotación.</p>
  </div>
</section>

<div class="div"></div>

<!-- ====== VII. ESPAÑA Y ANDALUCÍA ====== -->
<section class="section" id="espana">
  <div class="section-header">
    <div class="section-n">VII</div>
    <div class="section-head-text">
      <p class="label">Contexto nacional y autonómico</p>
      <h2>La Energía Hidráulica en España y Andalucía</h2>
    </div>
  </div>

  <div class="region-box">
    <h4>🇪🇸 España</h4>
    <p>España cuenta con una larga tradición hidroeléctrica gracias a su red de ríos y embalses. Dispone de <strong>más de un millar de centrales</strong> hidroeléctricas, siendo una de las principales fuentes renovables del país junto con la eólica y la solar fotovoltaica. Los grandes sistemas se concentran en las cuencas del <strong>Ebro, Duero, Tajo y Miño</strong>. Las centrales de bombeo están ganando protagonismo como complemento al auge de la energía solar y eólica.</p>
  </div>

  <div class="pros-cons" style="margin-top:14px;">
    <div class="pros">
      <h4>Ventajas en España</h4>
      <ul>
        <li>Renovable y de bajas emisiones</li>
        <li>Alta capacidad de respuesta a la demanda</li>
        <li>Bombeo como almacenamiento energético</li>
        <li>Infraestructura con larga vida útil</li>
      </ul>
    </div>
    <div class="cons">
      <h4>Limitaciones</h4>
      <ul>
        <li>Dependencia de las precipitaciones</li>
        <li>Impacto sobre ecosistemas fluviales</li>
        <li>Alteración de paisajes y hábitats</li>
        <li>Escasez de nuevos emplazamientos</li>
      </ul>
    </div>
  </div>

  <div class="region-box" style="margin-top:16px;">
    <h4>🌞 Andalucía</h4>
    <p>Andalucía no es la comunidad con mayor potencia hidroeléctrica —sus precipitaciones son menores que en el norte— pero cuenta con instalaciones significativas en las cuencas del <strong>Guadalquivir, Genil, Guadalhorce y Guadiana</strong>. Destacan el complejo hidroeléctrico de <strong>El Chorro</strong> (Málaga) con su central de bombeo, y los aprovechamientos ligados a los desniveles de <strong>Sierra Nevada</strong> (Granada). La estrategia energética andaluza prioriza la solar, pero la hidráulica mantiene un papel estratégico como <em>regulador y almacenamiento</em> del sistema eléctrico regional.</p>
  </div>

  <div class="callout" style="margin-top:20px;">
    <span class="icon">🔭</span>
    <p><strong>Perspectivas:</strong> El crecimiento de nueva hidráulica convencional será limitado por la disponibilidad hídrica y las restricciones ambientales. Sin embargo, las <strong>centrales de bombeo</strong> están llamadas a desempeñar un papel fundamental como almacenamiento de energía para integrar la creciente producción solar y eólica en la red.</p>
  </div>
</section>

<div class="div" style="margin-bottom:40px;"></div>

<!-- ====== VIII. CONCLUSIÓN ====== -->
<section id="conclusion">
  <div class="conclusion">
    <h2>Conclusión</h2>
    <p>La central hidroeléctrica es uno de los sistemas de generación eléctrica <strong>más completos, eficientes y longevos</strong> que existen. Integra principios fundamentales de la física (conservación de la energía, hidrodinámica, electromagnetismo) con ingeniería civil, mecánica y eléctrica en un proceso que transforma el agua embalsada en electricidad limpia con rendimientos superiores al 90%.</p>
    <p>Sus ocho elementos constitutivos —desde la presa hasta el parque de transformaciones— forman una cadena perfectamente diseñada en la que cada componente tiene una función crítica e irremplazable. La elección de la turbina adecuada, la correcta dimensión del canal, el control del golpe de ariete o la elevación de tensión son ejemplos de cómo la ingeniería resuelve problemas físicos reales.</p>
    <p>En un contexto de transición energética, la hidráulica no solo aporta energía renovable: las <strong>centrales de bombeo reversible</strong> se posicionan como la tecnología de almacenamiento más madura y eficiente del sistema eléctrico, complementando la variabilidad intrínseca de la energía solar y eólica. Su papel, lejos de decrecer, se vuelve más estratégico que nunca.</p>
    <div style="display:flex;gap:8px;flex-wrap:wrap;margin-top:16px;">
      <span class="badge" style="border-color:rgba(90,200,245,0.4);color:#a8dff5;">Energía renovable</span>
      <span class="badge" style="border-color:rgba(90,200,245,0.4);color:#a8dff5;">Rendimiento ~90%</span>
      <span class="badge" style="border-color:rgba(90,200,245,0.4);color:#a8dff5;">Regulable</span>
      <span class="badge" style="border-color:rgba(200,164,85,0.4);color:#e8c878;">Almacenamiento (bombeo)</span>
      <span class="badge" style="border-color:rgba(200,164,85,0.4);color:#e8c878;">Estratégica en España</span>
      <span class="badge" style="border-color:rgba(200,164,85,0.4);color:#e8c878;">0 emisiones directas</span>
    </div>
  </div>
</section>

</main>

<footer>
  <p><span>Tecnología e Ingeniería I</span> · 1.º Bachillerato B · Curso 2025–2026</p>
  <p style="margin-top:6px;">Víctor Morales Estrada · Ángel Sánchez López · Francisco José Barranco Fernández · Javier Palenzuela Sánchez</p>
  <p style="margin-top:6px;font-size:0.68rem;opacity:0.35;">Todos los esquemas y diagramas son de elaboración propia</p>
</footer>

</body>
</html>
