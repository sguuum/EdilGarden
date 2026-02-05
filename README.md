<html lang="it">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=0.44">

  <title>Edil Garden – Prodotti</title>

  <style>
    /* iOS / Safari fixes */
    * {
      -webkit-text-size-adjust: 121%;
    }

    /* evita riduzione automatica font */
    body {
      overflow-x: hidden;
      padding-top: env(safe-area-inset-top);
    }

    /* immagini e media responsive */
    img, video {
      max-width: 100%;
      height: auto;
      display: block;
    }

    /* smoother touch scrolling for galleries */
    .gallery {
      -webkit-overflow-scrolling: touch;
    }

    /* Hero mobile */
    @media (max-width: 600px) {
      .hero {
        font-size: 26px !important;
        height: 130px !important;
        padding-top: 30px !important;
        background-size: cover;
      }
      nav {
        padding: 10px 16px;
      }
    }

    /* ---------- qui continua il tuo CSS originale ---------- */

    body {
      margin: 0;
      font-family: system-ui, Arial, sans-serif;
      background: #f4f4f4;
      color: #213;
      padding-top: 68px;
    }

    /* MENU */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      background: #2d523c;
      padding: 15px 25px;
      display: flex;
      flex-wrap: wrap;
      gap: 25px;
      z-index: 1000;
    }


  nav a {
    color: white;
    text-decoration: none;
    font-weight: bold;
    cursor: pointer;
  }

  nav a:hover { text-decoration: underline; }

  /* HERO */
  .hero {
    width: 100%;
    height: 174px;
    background: url('https://www.casetteinlegnobrescia.it/casette-in-legno-top.jpg');
    background-position: center;
  

    display: flex;
    justify-content: center;
    color: white;
    text-shadow: 0 3px 8px rgba(0,0,0,0.6);
    font-size: 34,5px;
    font-weight: bold;
    letter-spacing: 0px;
    border-bottom: 3px solid #2d523c;
  }

  /* CONTENITORE */
  .container {
    max-width: 800px;
    margin: auto;
    padding: 25px;
  }

  h1 {
    color: #2d523c;
    margin-bottom: 25px;
    font-size: 32px;
  }

  h2 {
    color: #2d523c;
    margin-top: 20px;
  }

  /* GRIGLIA PRODOTTI */
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 20px;
  }

  .product {
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    cursor: pointer;
    transition: transform .15s ease;
  }

  .product:hover {
    transform: scale(1.03);
  }

  .product img {
    width: 100%;
    object-fit: cover;
  }

  .product-title {
    padding: 15px;
    font-weight: bold;
    color: #2d523c;
    text-align: center;
  }

  /* SEZIONI */
  .section {
    display: none;
    background: white;
    padding: 25px;
    border-radius: 12px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    margin-top: 30px;
  }

  .gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-top: 15px;
  }

  .gallery img {
    width: 300px;
    height: 200px;
    object-fit: cover;
    border-radius: 10px;
    cursor: zoom-in;
    box-shadow: 0 2px 6px rgba(0,0,0,0.15);
  }

  /* POPUP ZOOM */
  #zoom-popup {
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.85);
    display: none;
    justify-content: center;
    z-index: 9999;
  }

  #zoom-popup img {
    max-width: 90%;
    max-height: 90%;
    border-radius: 12px;
    cursor: zoom-out;
    transition: transform 0.15s ease;
  }

  .back-btn {
    margin-top: 20px;
    background: #2d523c;
    color: white;
    padding: 10px 18px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
}



:root{
  --side-color: #083826;
  --side-width: 90px;
  --content-maxw: 1150px;
  --page-vertical-gap: -16px;
  --content-bg: #ffffff;
  --content-radius: 23px;
  --content-shadow: 0 10px 30px rgba(0,0,0,0.20);
}

/* sfondo pagina verde scuro visibile ai lati */
html, body {
  height: 100%;
  margin: 0;
  background: var(--side-color);
  box-sizing: border-box;
}

/* bande laterali fisse */
body::before,
body::after {
  content: "";
  position: fixed;
  top: 0;
  bottom: 0;
  width: var(--side-width);
  background: var(--side-color);
  z-index: 0;
  pointer-events: none;
}
body::before { left: 0; }
body::after  { right: 0; }

/* contenitore centrale che racchiude tutto il sito */
.site-wrapper {
  position: relative;
  z-index: 1;
  max-width: var(--content-maxw);
  margin: var(--page-vertical-gap) auto;
  background: var(--content-bg);
  border-radius: var(--content-radius);
  box-shadow: var(--content-shadow);
  overflow: hidden;
  min-height: calc(100vh - (var(--page-vertical-gap) * 2));
  outline: var(--frame-border) solid var(--side-color);
  outline-offset: -12px;
}

/* se header è fixed, aggiusta il padding-top */
body.with-fixed-header .site-wrapper {
  padding-top: calc(30px + 70px); /* sostituisci 70px con l'altezza reale dell'header */
}

/* responsive */
@media (max-width: 1024px) { :root { --side-width: 0px; } }
@media (max-width: 600px) {
  :root { --side-width: 0px; }
  body::before, body::after { display: none; }
  .site-wrapper { margin: 12px; padding: 18px; min-height: auto; outline-offset: -8px; }
}


@media (max-width: 600px) {
  body {
    font-size: 16px;
    padding: 10px;
  }

  .container {
    width: 100%;
    padding: 10px;
  }

  img {
    max-width: 100%;
    height: auto;
  }

  .card {
    width: 100%;
    margin-bottom: 15px;
  }
}



</style>
</head>

<body>
 <div class="site-wrapper"> 
<!-- MENU --> 
<nav> <a onclick="showHome()">Home</a>
 </nav>



<!-- HERO -->
<div class="hero">EDIL GARDEN</div>

<div class="container">

  <!-- HOME CON TUTTI I PRODOTTI -->
  <div id="home">
    <h1>I nostri prodotti</h1>

    <div class="grid">

      <div class="product" onclick="openSection('casette')">
        <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/9fSQfWwX/20130426-181936(1).jpg">
        <div class="product-title">Casette da giardino</div>
      </div>

      <div class="product" onclick="openSection('porticati')">
        <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/porticati-index-2016.jpg">
        <div class="product-title">Porticati</div>
      </div>

      <div class="product" onclick="openSection('box-auto')">
        <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/box-auto-index-2016.jpg">
        <div class="product-title">Box Auto</div>
      </div>

      <div class="product" onclick="openSection('gazebo')">
        <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/gazebo-brescia-new-index.jpg">
        <div class="product-title">Gazebo</div>
      </div>

      <div class="product" onclick="openSection('pergole')">
        <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/pergole-in-legno-index-2016.jpg">
        <div class="product-title">Pergole</div>
      </div>

      <div class="product" onclick="openSection('pensiline')">
        <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/pensiline-brescia-new-index.jpg">
        <div class="product-title">Pensiline</div>
      </div>

      <div class="product" onclick="openSection('chioschi')">
        <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/chioschi-index-2016.jpg">
        <div class="product-title">Chioschi</div>
      </div>

      <div class="product" onclick="openSection('case-mobili')">
        <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/case-mobili-2-index-2016.jpg">
        <div class="product-title">Case mobili</div>
      </div>

      <div class="product" onclick="openSection('soluzioni-industriali')">
        <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/soluzioni-industriali-index.jpg">
        <div class="product-title">Soluzioni industriali</div>
      </div>

      <div class="product" onclick="openSection('case-abitabili')">
        <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/case-abitabili-index-2016.jpg">
        <div class="product-title">Case abitabili</div>
      </div>

    </div>
  </div>

  <!-- SEZIONE CASETTE + SOTTOCATEGORIE -->
  <div id="casette" class="section">
    <h2>Casette da giardino</h2>

    <div class="grid">

      <div class="product" onclick="openSub('casette-legno')">
        <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/casette-in-legno-index-2016.jpg">
        <div class="product-title">Case in legno</div>
      </div>

      <div class="product" onclick="openSub('casette-lamiera')">
        <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/casette-in-legno/casetta-salo-addossata-50-mm-2.jpg">
        <div class="product-title">Case in lamiera</div>
      </div>

      <div class="product" onclick="openSub('casette-intonacate')">
        <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FHM04Jt9/Whats-App-Image-2026-01-22-at-09-19-51.jpg">
        <div class="product-title">Case intonacate</div>
      </div>

    </div>

    <button class="back-btn" onclick="showHome()">Torna al menu</button>
  </div>

  <!-- SOTTOSEZIONE: CASE IN LEGNO -->
  <div id="casette-legno" class="section">
    <h2>Case in legno</h2>
    <div class="gallery">

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/J4J7t9CS/Whats-App-Image-2025-12-20-at-11-09-20.jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/D09NtjCg/Whats-App-Image-2025-12-20-at-11-09-20-(1).jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/PfC5nC3Z/Whats-App-Image-2025-12-20-at-11-09-20-(10).jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/RCWZxWsN/Whats-App-Image-2025-12-20-at-11-09-20-(11).jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/XNt7jnmB/Whats-App-Image-2025-12-20-at-11-09-20-(12).jpg"><p>5</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SQHNSm32/Whats-App-Image-2025-12-20-at-11-09-20-(13).jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/7PjYHqd2/Whats-App-Image-2025-12-20-at-11-09-20-(14).jpg"><p>7</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qBWMJpSC/Whats-App-Image-2025-12-20-at-11-09-20-(15).jpg"><p>8</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/HWFsYTRw/Whats-App-Image-2025-12-20-at-11-09-20-(16).jpg"><p>9</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/WpxbNsC7/Whats-App-Image-2025-12-20-at-11-09-20-(17).jpg"><p>10</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ZYXKbJ2V/Whats-App-Image-2025-12-20-at-11-09-20-(18).jpg"><p>11</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3rzJ83V1/Whats-App-Image-2025-12-20-at-11-09-20-(19).jpg"><p>12</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/gjC7fSM4/Whats-App-Image-2025-12-20-at-11-09-20-(2).jpg"><p>13</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/wMCrSfWh/Whats-App-Image-2025-12-20-at-11-09-20-(3).jpg"><p>14</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/4yD0rL8m/Whats-App-Image-2025-12-20-at-11-09-20-(5).jpg"><p>15</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ZnGQ17fP/Whats-App-Image-2025-12-20-at-11-09-20-(6).jpg"><p>16</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/2ystPcH9/Whats-App-Image-2025-12-20-at-11-09-20-(7).jpg"><p>17</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qBNvHNbM/Whats-App-Image-2025-12-20-at-11-09-20-(8).jpg"><p>18</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/1R8318CR/Whats-App-Image-2025-12-20-at-11-09-20-(9).jpg"><p>19</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/7Y7Pbpyq/Whats-App-Image-2026-01-08-at-08-26-42.jpg"><p>20</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/TYm2hZXP/Whats-App-Image-2026-01-08-at-08-26-52.jpg"><p>21</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vZsYn3QG/Whats-App-Image-2026-01-08-at-08-26-54.jpg"><p>22</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/HkgYMBpb/Whats-App-Image-2026-01-08-at-08-26-59.jpg"><p>23</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/g2HYH8Jh/Whats-App-Image-2026-01-08-at-08-27-01.jpg"><p>24</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/9QYWYZMY/Whats-App-Image-2026-01-08-at-08-27-05.jpg"><p>25</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/6pf9fn3H/Whats-App-Image-2026-01-08-at-08-27-17.jpg"><p>26</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ht1S1TvW/Whats-App-Image-2026-01-08-at-08-27-19.jpg"><p>27</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/QMNj4C9P/Whats-App-Image-2026-01-08-at-08-27-20.jpg"><p>28</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/25jCcybP/Whats-App-Image-2026-01-08-at-08-27-32.jpg"><p>29</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fbWM2ySR/Whats-App-Image-2026-01-08-at-08-27-35.jpg"><p>30</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fbHD6sYR/Whats-App-Image-2026-01-08-at-08-27-37.jpg"><p>31</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/CKvSW0bm/Whats-App-Image-2026-01-08-at-08-27-50.jpg"><p>32</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3RdYhqZb/Whats-App-Image-2026-01-08-at-08-27-53.jpg"><p>33</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/26VrYtwD/Whats-App-Image-2026-01-08-at-08-27-56.jpg"><p>34</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/0QFxyCtF/Whats-App-Image-2026-01-08-at-08-27-58.jpg"><p>35</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/859DzbKS/Whats-App-Image-2026-01-08-at-08-27-59.jpg"><p>36</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sXqygJ62/Whats-App-Image-2026-01-08-at-08-28-01.jpg"><p>37</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/pT4xLBGn/Whats-App-Image-2026-01-08-at-08-28-03.jpg"><p>38</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qqKrhCSz/Whats-App-Image-2026-01-08-at-08-28-08.jpg"><p>39</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/J0X8DBvy/Whats-App-Image-2026-01-08-at-08-28-10.jpg"><p>40</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/KjTbkgwt/Whats-App-Image-2026-01-08-at-08-28-12.jpg"><p>41</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/gjhpX6QN/Whats-App-Image-2026-01-08-at-08-28-14.jpg"><p>42</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/KjTbkgw9/Whats-App-Image-2026-01-08-at-08-28-16.jpg"><p>43</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3NGh4DVb/Whats-App-Image-2026-01-08-at-08-28-25.jpg"><p>44</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ZYv4D1nJ/Whats-App-Image-2026-01-08-at-08-28-28.jpg"><p>45</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8kfNnqck/Whats-App-Image-2026-01-08-at-08-28-30.jpg"><p>46</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/52NkcLSh/Whats-App-Image-2026-01-22-at-08-26-25.jpg"><p>47</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fR2qMyHk/Whats-App-Image-2026-01-22-at-08-26-53.jpg"><p>48</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Dwjp70Cb/Whats-App-Image-2026-01-22-at-08-26-53-(1).jpg"><p>49</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fR2qMyH3/Whats-App-Image-2026-01-22-at-08-26-53-(2).jpg"><p>50</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/tgsSJbfR/Whats-App-Image-2026-01-22-at-08-26-53-(3).jpg"><p>51</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8Cxyr3QZ/Whats-App-Image-2026-01-22-at-08-26-54.jpg"><p>52</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/g0xSjp53/Whats-App-Image-2026-01-22-at-08-26-54-(1).jpg"><p>53</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/xdXx8Q7R/Whats-App-Image-2026-01-22-at-08-26-54-(2).jpg"><p>54</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/1z8CXSTv/Whats-App-Image-2026-01-22-at-08-26-54-(3).jpg"><p>55</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/B6Dm5gJS/Whats-App-Image-2026-01-22-at-08-26-54-(4).jpg"><p>56</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/k5LjtZ3N/Whats-App-Image-2026-01-22-at-08-26-54-(5).jpg"><p>57</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/JnJp3qRb/Whats-App-Image-2026-01-22-at-08-26-55.jpg"><p>58</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bv462Mc4/Whats-App-Image-2026-01-22-at-08-26-55-(1).jpg"><p>59</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/1zbWNT1S/Whats-App-Image-2026-01-22-at-08-26-55-(2).jpg"><p>60</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vB907zGw/Whats-App-Image-2026-01-22-at-08-26-55-(3).jpg"><p>61</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/L4tynNyL/Whats-App-Image-2026-01-22-at-08-26-55-(4).jpg"><p>62</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ncn37Bgx/Whats-App-Image-2026-01-22-at-08-26-56.jpg"><p>63</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8cStZ6CF/Whats-App-Image-2026-01-22-at-08-26-56-(1).jpg"><p>64</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/xT96HMh8/Whats-App-Image-2026-01-22-at-08-26-56-(2).jpg"><p>65</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3NF9VxyP/Whats-App-Image-2026-01-22-at-08-26-56-(3).jpg"><p>66</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vTtXkZgd/Whats-App-Image-2026-01-22-at-08-26-56-(4).jpg"><p>67</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/520pK1xM/Whats-App-Image-2026-01-22-at-08-26-56-(5).jpg"><p>68</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/VLzKMnT3/Whats-App-Image-2026-01-22-at-08-26-56-(6).jpg"><p>69</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/t4MkLfTg/Whats-App-Image-2026-01-22-at-08-26-57.jpg"><p>70</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/cLbhVjJV/Whats-App-Image-2026-01-22-at-08-26-57-(1).jpg"><p>71</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sDKwJ1CQ/Whats-App-Image-2026-01-22-at-08-26-57-(2).jpg"><p>72</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/9F1JBzHw/Whats-App-Image-2026-01-22-at-08-26-57-(3).jpg"><p>73</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/NjMbCYQJ/Whats-App-Image-2026-01-22-at-08-26-57-(4).jpg"><p>74</p>



    </div>
    <button class="back-btn" onclick="openSection('casette')">Torna alle casette</button>
  </div>

  <!-- SOTTOSEZIONE: CASE IN LAMIERA -->
  <div id="casette-lamiera" class="section">
    <h2>Case in lamiera</h2>
    <div class="gallery">

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Jn0yDP1C/Whats-App-Image-2025-12-20-at-11-09-20-(20).jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/k4GV6fn3/Whats-App-Image-2025-12-20-at-11-09-20-(24).jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fLy3tBM1/Whats-App-Image-2025-12-20-at-11-09-20-(4).jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/xC8kJt97/Whats-App-Image-2026-01-08-at-08-26-44.jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/76hCGmx4/Whats-App-Image-2026-01-08-at-08-26-47.jpg"><p>5</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/j52WwZsq/Whats-App-Image-2026-01-08-at-08-26-48.jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/xC8kJt01/Whats-App-Image-2026-01-08-at-08-26-50.jpg"><p>7</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/tTcshWTQ/Whats-App-Image-2026-01-08-at-08-27-34.jpg"><p>8</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vBK4WfBb/Whats-App-Image-2026-01-08-at-08-27-54.jpg"><p>9</p>


<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/CMPcjW4d/Whats-App-Image-2026-01-22-at-08-22-04.jpg"><p>12</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/6qmztvQc/Whats-App-Image-2026-01-22-at-08-22-04-(1).jpg"><p>13</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8kKZhqbz/Whats-App-Image-2026-01-22-at-08-22-04-(2).jpg"><p>14</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/g0HDr5J9/Whats-App-Image-2026-01-22-at-08-22-05.jpg"><p>15</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ZKWVjVf0/Whats-App-Image-2026-01-22-at-08-22-05-(1).jpg"><p>16</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/g0HDr5Jz/Whats-App-Image-2026-01-22-at-08-22-05-(2).jpg"><p>17</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/k5vcDZ45/Whats-App-Image-2026-01-22-at-08-22-05-(3).jpg"><p>18</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/26jxWwbL/Whats-App-Image-2026-01-22-at-08-22-06.jpg"><p>19</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/257w3J6b/Whats-App-Image-2026-01-22-at-08-22-06-(1).jpg"><p>20</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/TwkJJDgV/Whats-App-Image-2026-01-22-at-08-22-07.jpg"><p>21</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/k4MySc68/Whats-App-Image-2026-01-22-at-08-22-07-(1).jpg"><p>22</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fLWvdKtm/Whats-App-Image-2026-01-22-at-08-22-07-(2).jpg"><p>23</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/k4MySc6f/Whats-App-Image-2026-01-22-at-08-22-07-(3).jpg"><p>24</p>


    </div>
    <button class="back-btn" onclick="openSection('casette')">Torna alle casette</button>
  </div>

  <!-- SOTTOSEZIONE: CASE INTONACATE -->
  <div id="casette-intonacate" class="section">
    <h2>Case intonacate</h2>
    <div class="gallery">

  <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fy7fz3rY/Whats-App-Image-2026-01-08-at-08-27-07.jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fWYKjFT1/Whats-App-Image-2026-01-08-at-08-27-09.jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/RCwRQ8V8/Whats-App-Image-2026-01-08-at-08-27-12.jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Df1gdDwK/Whats-App-Image-2026-01-08-at-08-27-16.jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nVqkY5hb/Whats-App-Image-2026-01-08-at-08-27-27.jpg"><p>5</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/pVKZY7Lv/Whats-App-Image-2026-01-08-at-08-27-28.jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/66C0LSpW/Whats-App-Image-2026-01-08-at-08-27-29.jpg"><p>7</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/L6RVyTJ2/Whats-App-Image-2026-01-08-at-08-27-31.jpg"><p>8</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Qxsq6bFD/Whats-App-Image-2026-01-08-at-08-28-19.jpg"><p>9</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/02xCtfz9/Whats-App-Image-2026-01-08-at-08-28-23.jpg"><p>10</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FHM04Jt9/Whats-App-Image-2026-01-22-at-09-19-51.jpg"><p>11</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/43pVNNZg/Whats-App-Image-2026-01-22-at-09-19-52.jpg"><p>12</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3w2mJJ77/Whats-App-Image-2026-01-22-at-09-19-52-(1).jpg"><p>13</p>


<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/g038kkdz/Whats-App-Image-2026-01-22-at-09-24-17.jpg"><p>16</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FK03ssms/Whats-App-Image-2026-01-22-at-09-24-18.jpg"><p>17</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bv1kNN8J/Whats-App-Image-2026-01-22-at-09-24-18-(1).jpg"><p>18</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/s257DDyM/Whats-App-Image-2026-01-22-at-09-24-18-(2).jpg"><p>19</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/wBDLTTHR/Whats-App-Image-2026-01-22-at-09-24-18-(3).jpg"><p>20</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/XJdgBkbw/Whats-App-Image-2026-01-22-at-09-45-20.jpg"><p>22</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/NMmx2kcR/Whats-App-Image-2026-01-22-at-09-45-20-(1).jpg"><p>23</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/1twKVrQG/Whats-App-Image-2026-01-22-at-09-45-20-(2).jpg"><p>24</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FR3xkV4g/Whats-App-Image-2026-01-22-at-09-45-20-(3).jpg"><p>25</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8PcgM77L/Whats-App-Image-2026-01-22-at-10-01-50.jpg"><p>26</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bNrfkZZs/Whats-App-Image-2026-01-22-at-10-01-50-(1).jpg"><p>27</p>

    </div>
    <button class="back-btn" onclick="openSection('casette')">Torna alle casette</button>
  </div>

  

  <div id="porticati" class="section">
    <h2>Porticati</h2>
    <div class="gallery">
     
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Yq1Z1tbs/Whats-App-Image-2026-01-22-at-08-38-46.jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/MKyNyz9w/Whats-App-Image-2026-01-22-at-08-38-46-(1).jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/tChwh9BC/Whats-App-Image-2026-01-22-at-08-38-46-(2).jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/K8xVfCWF/Whats-App-Image-2026-01-22-at-08-38-46-(3).jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/pLR7C3Sd/Whats-App-Image-2026-01-22-at-08-38-46-(4).jpg"><p>5</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/6ptScFPr/Whats-App-Image-2026-01-22-at-08-38-47.jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/htsY5pFC/Whats-App-Image-2026-01-22-at-08-38-47-(1).jpg"><p>7</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/zG7Qc0mx/Whats-App-Image-2026-01-22-at-08-38-48.jpg"><p>8</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/R00Y5K92/Whats-App-Image-2026-01-22-at-08-38-48-(1).jpg"><p>9</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/6QQPJnwk/Whats-App-Image-2026-01-22-at-08-38-48-(2).jpg"><p>10</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/s22Ld7sy/Whats-App-Image-2026-01-22-at-08-38-48-(3).jpg"><p>11</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/4330kVsy/Whats-App-Image-2026-01-22-at-08-38-48-(4).jpg"><p>12</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SsJH88vZ/Whats-App-Image-2026-01-22-at-08-38-49.jpg"><p>13</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/mDJJSkxZ/Whats-App-Image-2026-01-22-at-08-38-49-(1).jpg"><p>14</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/DZHHcZ99/Whats-App-Image-2026-01-22-at-08-38-49-(2).jpg"><p>15</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/26MMxypS/Whats-App-Image-2026-01-22-at-08-38-49-(3).jpg"><p>16</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/MTNNYHkK/Whats-App-Image-2026-01-22-at-08-38-49-(4).jpg"><p>17</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FR88xzt7/Whats-App-Image-2026-01-22-at-08-38-50.jpg"><p>18</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8cv3XGDm/Whats-App-Image-2026-01-22-at-08-38-50-(1).jpg"><p>19</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/5yzGKJ17/Whats-App-Image-2026-01-22-at-08-38-50-(2).jpg"><p>20</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/7PJpZ378/Whats-App-Image-2026-01-22-at-08-38-50-(3).jpg"><p>21</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ZYv1583n/Whats-App-Image-2026-01-22-at-08-38-50-(4).jpg"><p>22</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/VLy2rJBr/Whats-App-Image-2026-01-22-at-08-38-51.jpg"><p>23</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/QxLv9Fk1/Whats-App-Image-2026-01-22-at-08-38-51-(1).jpg"><p>24</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/gk91Xxq4/Whats-App-Image-2026-01-22-at-08-38-51-(2).jpg"><p>25</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qM8S8pjb/Whats-App-Image-2026-01-22-at-08-38-52.jpg"><p>26</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/tChwh9BQ/Whats-App-Image-2026-01-22-at-08-38-52-(1).jpg"><p>27</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/MG3wyvZz/Whats_App_Image_2026_01_09_at_16_04_15_(1).jpg"><p>28</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/1tgQMs40/Whats_App_Image_2026_01_09_at_16_04_15_(4).jpg"><p>29</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/yYhzLf6J/Whats_App_Image_2026_01_09_at_16_04_16.jpg"><p>30</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/64WPCd1N/Whats-App-Image-2026-01-09-at-16-04-16-(1).jpg"><p>31</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/zXYrSmNB/Whats_App_Image_2026_01_09_at_16_04_16_(2).jpg"><p>32</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/zXw1xdDM/Whats_App_Image_2026_01_09_at_16_04_17_(2).jpg"><p>33</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ykrGS3m2/Whats-App-Image-2026-01-09-at-16-04-18-(2).jpg"><p>34</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/porticato-in-legno-lamellare-2014.jpg"><p>35</p>

<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/porticati/porticato-con-struttura-in-legno-lamellare-2016.jpg"><p>36</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/arcover-legno-edilgarden.jpg"><p>37</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/arcover-per-auto.jpg"><p>38</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/arcover-auto-3-new.jpg"><p>39</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/arcover-auto-2.jpg"><p>40</p>

<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/arcover-posti-auto-new.jpg"><p>41</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/arcover-brescia.jpg"><p>42</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/arcover-edilgarden.jpg"><p>43</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/porticato-completo-di-pannelli-frangivento.jpg"><p>44</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/porticato-completo-di-pannelli-frangivento-2.jpg"><p>45</p>

<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/porticato-completo-di-casetta-ripostiglio.jpg"><p>46</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/arcover-legno-auto/porticato-in-legno-lamellare-2014.jpg"><p>47</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sMqbbG1s/Whats-App-Image-2026-01-09-at-16-00-14.jpg"><p>48</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/WdhQ9wNx/Whats-App-Image-2026-01-09-at-16-00-14-(1).jpg"><p>49</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/WdhQ9wpc/Whats-App-Image-2026-01-09-at-16-00-14-(3).jpg"><p>50</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/PCPB6Qff/Whats-App-Image-2026-01-09-at-16-00-14-(5).jpg"><p>51</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/WdCxxqtG/Whats-App-Image-2026-01-09-at-16-00-15.jpg"><p>52</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/MnNggfXT/Whats-App-Image-2026-01-09-at-16-00-15-(1).jpg"><p>53</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/TKFBB5hy/Whats-App-Image-2026-01-09-at-16-00-15-(3).jpg"><p>54</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/9DKssw-zw/Whats-App-Image-2026-01-09-at-16-00-15-(4).jpg"><p>55</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qNSW-W6g8/Whats-App-Image-2026-01-09-at-16-00-15-(5).jpg"><p>56</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Sn3HHYj7/Whats-App-Image-2026-01-09-at-16-03-51.jpg"><p>57</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/62LS7Hc2/Whats-App-Image-2026-01-09-at-16-04-14.jpg"><p>58</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/f3d1sW-03/Whats-App-Image-2026-01-09-at-16-04-14-(1).jpg"><p>59</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/S275XZdq/Whats-App-Image-2026-01-09-at-16-04-14-(3).jpg"><p>60</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/7GMcCB90/Whats-App-Image-2026-01-09-at-16-04-15-(5).jpg"><p>61</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/zXYrSmNB/Whats_App_Image_2026_01_09_at_16_04_16_(2).jpg"><p>63</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rzj3MPzb/Whats-App-Image-2026-01-09-at-16-04-16-(4).jpg"><p>64</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/14B2sjfQ/Whats-App-Image-2026-01-09-at-16-04-16-(5).jpg"><p>65</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/BXwz1PTP/Whats-App-Image-2026-01-09-at-16-04-17-(3).jpg"><p>67</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/RNbYnJ15/Whats-App-Image-2026-01-09-at-16-04-18.jpg"><p>68</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/gnB76LVg/Whats-App-Image-2026-01-09-at-16-04-18-(1).jpg"><p>69</p>

    </div>
    <button class="back-btn" onclick="showHome()">Torna al menu</button>
  </div>

  <div id="box-auto" class="section">
    <h2>Box Auto</h2>
    <div class="gallery">

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Cx0tJd13/Whats-App-Image-2026-01-22-at-09-55-36.jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3xZqq70Y/Whats-App-Image-2026-01-22-at-09-55-37.jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SxGPPq2T/Whats-App-Image-2026-01-22-at-09-55-37-(1).jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/k5XH3ZWb/Whats-App-Image-2026-01-22-at-09-55-38.jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/BvQz9y2t/Whats-App-Image-2026-01-22-at-09-55-38-(1).jpg"><p>5</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nLRPHk1Y/Whats-App-Image-2026-01-22-at-09-55-40.jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/GphfwNvK/Whats-App-Image-2026-01-22-at-09-55-40-(1).jpg"><p>7</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/QdgmMbjM/Whats-App-Image-2026-01-22-at-09-55-41.jpg"><p>8</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/P5nKhcnt/Whats-App-Image-2026-01-22-at-09-55-41-(3).jpg"><p>9</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/7Z19LVqJ/Whats-App-Image-2026-01-22-at-09-55-42.jpg"><p>10</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/RZxG98xN/Whats-App-Image-2026-01-22-at-09-55-42-(1).jpg"><p>11</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/t4GDyfGs/Whats-App-Image-2026-01-22-at-09-55-42-(2).jpg"><p>12</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/P5nKhcnv/Whats-App-Image-2026-01-22-at-09-55-42-(3).jpg"><p>13</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/6pVcQ0B7/Whats-App-Image-2026-01-22-at-09-55-42-(4).jpg"><p>14</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/N0g42H0z/Whats-App-Image-2026-01-22-at-09-55-43.jpg"><p>15</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fR7CbKM7/Whats-App-Image-2026-01-22-at-09-55-43-(1).jpg"><p>16</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Hk0zL2TS/Whats-App-Image-2026-01-22-at-09-55-43-(2).jpg"><p>17</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/L8kDsTmQ/Whats-App-Image-2026-01-22-at-09-55-43-(3).jpg"><p>18</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Jz3xhqRF/Whats-App-Image-2026-01-22-at-09-55-43-(4).jpg"><p>19</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/xd0RNzdw/Whats-App-Image-2026-01-22-at-09-55-44.jpg"><p>20</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bYK4Dmj8/Whats-App-Image-2026-01-22-at-09-58-03.jpg"><p>21</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/t7Qdq1wb/Whats-App-Image-2026-01-22-at-09-58-04.jpg"><p>22</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ZqVL85B4/Whats-App-Image-2026-01-22-at-09-58-04-(1).jpg"><p>23</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/15w2pD9q/Whats-App-Image-2026-01-22-at-09-58-04-(2).jpg"><p>24</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/tTJN2GWB/Whats-App-Image-2026-01-22-at-09-58-04-(3).jpg"><p>25</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/GtsJnPMp/Whats-App-Image-2026-01-22-at-09-58-04-(4).jpg"><p>26</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/D0bd3QCv/Whats-App-Image-2026-01-22-at-09-58-04-(5).jpg"><p>27</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/xjWBJ6S2/Whats-App-Image-2026-01-22-at-09-58-04-(6).jpg"><p>28</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/6pKSzT3m/Whats-App-Image-2026-01-22-at-09-58-05.jpg"><p>29</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/28hM4nzB/Whats-App-Image-2026-01-22-at-09-58-05-(1).jpg"><p>30</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SKPVZHzR/20130130-121546(2)-Copia.jpg"><p>31</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/tRWD5SR0/20130130-124417.jpg"><p>32</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ncx2w4MB/20130520-122325(1)-Copia.jpg"><p>33</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/jqPvXgqw/20130606-181351(1)-Copia.jpg"><p>34</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/TYx0HVhb/20130606-182325(2)-Copia.jpg"><p>35</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Jhs5BKYQ/20130704-105034-Copia-(2).jpg"><p>36</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nLXGQTST/20130912-184242-Copia-(2).jpg"><p>37</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FKYVJGn5/20140407-181558-Copia-(2).jpg"><p>38</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/PqCQ8KFh/20140808-165520-Copia-(2).jpg"><p>39</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3NTXVh8L/20140808-184423.jpg"><p>40</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fWcjXV5s/20140808-184523-Copia.jpg"><p>41</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/15y0KyYF/20140808-184607.jpg"><p>42</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/jqHQNDvN/20140811-145542-Copia-(2).jpg"><p>43</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bNLxC4Km/20140811-150354.jpg"><p>44</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/BnVxsHZc/20141211-151512.jpg"><p>45</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rpR5psK0/20141219-130515.jpg"><p>46</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3RMm0hv8/20150112-165300.jpg"><p>47</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/RFrKJmHw/20150113-153532.jpg"><p>48</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/264v4tQM/20150225-174543.jpg"><p>49</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vH89V3cj/20150311-182046.jpg"><p>50</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qMBn3jz8/20150311-182116.jpg"><p>51</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/28HWFhWr/20150330-192014.jpg"><p>52</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/5NPzqLzY/20150330-192331.jpg"><p>53</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/JnWH4Qfp/20150511-185003.jpg"><p>54</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/63L27vK0/20150511-185802.jpg"><p>55</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ZRFB9dZ5/20150623-175532.jpg"><p>56</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/PJXL15rd/20150705-105453.jpg"><p>57</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/x8fkL1TX/20151102-163003.jpg"><p>58</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sfmGs7wv/20151109-165543.jpg"><p>59</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/L4Dg2LNN/20151111-162925.jpg"><p>60</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/44PHsVB8/20151111-163134.jpg"><p>61</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/CLKB152V/20151117-153447.jpg"><p>62</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/kXhVt9rS/20151117-154129.jpg"><p>63</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Z5GCVcKf/20151126-142113.jpg"><p>64</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/N0RLVHKB/20151126-142153.jpg"><p>65</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/MTxX8pRJ/20151126-142301.jpg"><p>66</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/d3V1LN4t/20151126-154805.jpg"><p>67</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/MZ9Hhxpn/20151126-154842.jpg"><p>68</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/5NjyJGXk/20151216-145810.jpg"><p>69</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/7Z2LG2Mz/20160107-151727.jpg"><p>70</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bwtvDtHt/20160107-151737.jpg"><p>71</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/wBYjhjw8/20160107-161735.jpg"><p>72</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/yNC8F8Ld/20160129-102553.jpg"><p>73</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/KzZcHsXQ/20160129-102641.jpg"><p>74</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/pT2V61bP/20160727-170851.jpg"><p>75</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/05X5VfVn/20160727-171109.jpg"><p>76</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/026kFw31/20160730-123744.jpg"><p>77</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/L8LH6M2w/20161201-160026.jpg"><p>78</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/T3gRYXT8/20161206-152005.jpg"><p>79</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/GpRb4SpF/20161206-153149.jpg"><p>80</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/LX6RTYLd/20161206-161101.jpg"><p>81</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/V6GwHfWj/20161206-161435.jpg"><p>82</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/TYWxCXLK/20161206-162422.jpg"><p>83</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/WbJVXPF2/20161214-131441.jpg"><p>84</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/zGZrQPK2/20161214-132004.jpg"><p>85</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Nj6cv7xh/20161217-153729.jpg"><p>86</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FKGX7rqc/20170116-121303.jpg"><p>87</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/500dvcW9/20170125-163436.jpg"><p>88</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Kj6ddRK6/20170206-101929.jpg"><p>89</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Y05JJhGv/20170208-155403.jpg"><p>90</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/v8CTQh5G/20170208-155912.jpg"><p>91</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8kxc14Lc/20170215-114923.jpg"><p>92</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Njc0X0J9/20170728-104857.jpg"><p>93</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nLVcdPfq/20171116-091922.jpg"><p>94</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Xv2NtkVj/20171117-164647.jpg"><p>95</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/9MrX2wM1/20171213-122847.jpg"><p>96</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/d3CqkMGD/20171213-123204.jpg"><p>97</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/j2fswVy4/20171222-155539.jpg"><p>98</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/RZ4MFDhB/20180119-123022.jpg"><p>99</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/P5yd8QvQ/20180208-132456.jpg"><p>100</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/DzznQ4q7/20180905-161849.jpg"><p>101</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/9QCWMn0q/foto-2.jpg"><p>102</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/mr6RmZwF/foto-edilgarde1-005.jpg"><p>103</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FRMvQPwQ/IMGP0998-Copia-(2).jpg"><p>104</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/GtvC3F1v/IMGP1007.jpg"><p>105</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/dtmYzjBp/IMGP1093.jpg"><p>106</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/P5XjhvV5/IMGP1099-Copia-(2).jpg"><p>107</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/65LXDf0F/IMGP1516.jpg"><p>108</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vHLspthY/IMGP1653.jpg"><p>109</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/t4qjynvs/IMGP1667.jpg"><p>110</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/g2zWdLt6/IMGP1679.jpg"><p>111</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/DZXV5r0H/Immagine-1595.jpg"><p>112</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/WzLBydJ2/Immagine-1599.jpg"><p>113</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8zpSDfXB/Immagine-340.jpg"><p>114</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/DwxKzfRs/Immagine-386.jpg"><p>115</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Mp98GZgD/Immagine-392.jpg"><p>116</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/52sMt9Ds/Immagine-399.jpg"><p>117</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/pTFNkfr7/Immagine-4267.jpg"><p>118</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/26ZpTQ3r/Immagine-5825.jpg"><p>119</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/XqfR6nw9/l-287.jpg"><p>120</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rs1B2qSn/P1010007.jpg"><p>121</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/h4VWd1Hc/P1010008.jpg"><p>122</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bY1ct9Ks/P1010064.jpg"><p>123</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/NGRqHkWm/P1010077.jpg"><p>124</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SNq07zh7/P1010079.jpg"><p>125</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8PD8BrSt/P1010097.jpg"><p>126</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/WbjR6JVL/Screenshot-2014-09-21-23-57-09.png"><p>127</p>



    </div>
    <button class="back-btn" onclick="showHome()">Torna al menu</button>
  </div>

  <div id="gazebo" class="section">
    <h2>Gazebo</h2>
    <div class="gallery">

      <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/PrYcHdZd/Whats-App-Image-2026-01-22-at-08-47-21.jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/CMWt9RRv/Whats-App-Image-2026-01-22-at-08-47-21-(1).jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/W3xWRy1c/Whats-App-Image-2026-01-22-at-08-47-21-(2).jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/T3xsYBqp/Whats-App-Image-2026-01-22-at-08-47-21-(3).jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/50X7RJ1h/Whats-App-Image-2026-01-22-at-08-47-22.jpg"><p>5</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/DwhNyRdT/Whats-App-Image-2026-01-22-at-08-47-22-(1).jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Njxzybp7/Whats-App-Image-2026-01-22-at-08-47-22-(2).jpg"><p>7</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8zb0FwtR/Whats-App-Image-2026-01-22-at-08-47-22-(3).jpg"><p>8</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/BnCV8NMz/Whats-App-Image-2026-01-22-at-08-47-22-(4).jpg"><p>9</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/W3dWHVjX/Whats-App-Image-2026-01-22-at-08-47-22-(5).jpg"><p>10</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/mZFp3Tm4/Whats-App-Image-2026-01-22-at-08-47-23.jpg"><p>11</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/9MD8n2VP/Whats-App-Image-2026-01-22-at-08-47-23-(1).jpg"><p>12</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/QMt0FDFY/Whats-App-Image-2026-01-22-at-08-47-23-(2).jpg"><p>13</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/x19sSMn0/Whats-App-Image-2026-01-22-at-08-47-24.jpg"><p>14</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qMVbjWFj/Whats-App-Image-2026-01-22-at-08-47-24-(1).jpg"><p>15</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/d1sLYVgZ/20140811-111551.jpg"><p>16</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FH0RkS4s/20140811-111611.jpg"><p>17</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/43Z363fx/20140811-111627.jpg"><p>18</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/4N7nZM2V/20140811-111815.jpg"><p>19</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/JhmhNhrt/20140811-144213.jpg"><p>20</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rpJwQLsB/20140811-144300.jpg"><p>21</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/W4Xs06YK/20140811-144454.jpg"><p>22</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qRq4wh98/20140811-144531.jpg"><p>23</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/cJXdfM5q/20140811-144610.jpg"><p>24</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/TwsG4260/20140811-150044.jpg"><p>25</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/pLv9ZCkZ/20140811-150056.jpg"><p>26</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fW6S3D96/20160615-134459.jpg"><p>27</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Jz8yqxKr/20160615-134534.jpg"><p>28</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vZy1zhX7/20160615-134700.jpg"><p>29</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/HktrPMPh/20180614-163116.jpg"><p>30</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/6Q58sQkJ/20180614-163246.jpg"><p>31</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/s26v3rzn/20180614-163304.jpg"><p>32</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/NMKLMzG8/20180614-163316.jpg"><p>33</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/HxFn79Vr/20180614-163438.jpg"><p>34</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/J0Jn3HkQ/20180904-145621.jpg"><p>35</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/J7BGCv2k/20180904-183754.jpg"><p>36</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/G3sHnV5G/20180904-183901.jpg"><p>37</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/PrWJPZhn/DSC00341.jpg"><p>38</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vHrTc9Ms/IMGP0940.jpg"><p>39</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nc4rC7Zj/IMGP0946.jpg"><p>40</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sDYxvSyh/IMGP0974.jpg"><p>41</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rwqmWmF5/IMGP0975.jpg"><p>42</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vZXmvs4Q/IMGP1059.jpg"><p>43</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/BnNvC0jJ/IMGP1060.jpg"><p>44</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/7L6ZsWzf/IMGP1062.jpg"><p>45</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/R0FZsDt0/IMGP1632.jpg"><p>46</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/j5ndKnZr/Immagine-1411.jpg"><p>47</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rs6ypyPq/Immagine-1414.jpg"><p>48</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/0jpkKgTc/Immagine-2676.jpg"><p>49</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/25K8P7d1/Immagine-430.jpg"><p>50</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/jjFdG46h/Immagine-433.jpg"><p>51</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/CKQLWsCX/Immagine-473.jpg"><p>52</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/d3MQ0Qxy/P1010037.jpg"><p>53</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FzjrktM0/P1010136.jpg"><p>54</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nrvF98yN/PC190065.jpg"><p>55</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/yxF134qH/PC220127.jpg"><p>56</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/15rR9Qc6/rosolina-2011-238.jpg"><p>57</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/CxMh5QmD/rosolina-2011-241.jpg"><p>58</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Wz010tWM/Whats-App-Image-2026-01-22-at-09-27-17.jpg"><p>59</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FFSRMnrr/Whats-App-Image-2026-01-22-at-09-27-18.jpg"><p>60</p>

    </div>
    <button class="back-btn" onclick="showHome()">Torna al menu</button>
  </div>

  <div id="pergole" class="section">
    <h2>Pergole</h2>
    <div class="gallery">

      <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/d0LSt1B1/20130228-154949(1).jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/2SHKDv4L/20140811-111551.jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/JzT2LJbD/20140811-111611.jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/y8fbH9F9/20140811-111948.jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/k5BhX4cB/20140811-144224.jpg"><p>5</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bvsFNJTZ/20140811-144300.jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/hGf3Pjrz/20140811-144531.jpg"><p>7</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vmk21sqC/20141224-113834.jpg"><p>8</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/zvSxPRz1/20141224-113857.jpg"><p>9</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/VLmG04gJ/20141230-165702.jpg"><p>10</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Ghd7TzKD/20141230-165756.jpg"><p>11</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bwvm3J4V/20141230-165846.jpg"><p>12</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nhL30z6z/20141230-165934.jpg"><p>13</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sg0w8zrW/20141230-170119.jpg"><p>14</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/YSGbBPrY/20150608-201201.jpg"><p>15</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/s2QwCLjm/20150608-201226.jpg"><p>16</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/5tYnWr9W/20150608-201253.jpg"><p>17</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/cHfhr883/20150608-201409.jpg"><p>18</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/zvjkkZj9/20150608-201417.jpg"><p>19</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/DyxgJhm5/20150608-201538.jpg"><p>20</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8PZHJGjg/20150608-201603.jpg"><p>21</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/htw1s0Lt/20150608-202258.jpg"><p>22</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SRy6R14S/20150608-202405.jpg"><p>23</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/C5mjqCMf/20150608-202459.jpg"><p>24</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3JxjHq9B/20150720-145615.jpg"><p>25</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/XYZwryRJ/20150807-105323.jpg"><p>26</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/9QvyZQ2N/20160622-204918.jpg"><p>27</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/MGVVDJZ3/20170802-112159.jpg"><p>28</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/KzbLppRK/20170802-112328.jpg"><p>29</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/TwcbzjDz/20170802-112639.jpg"><p>30</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/5NrzW26p/20170802-113558.jpg"><p>31</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/13Nqm1FQ/20171005-160201.jpg"><p>32</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nzTsRHy5/20171005-160209.jpg"><p>33</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Wz3dxBjg/20171005-160228.jpg"><p>34</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fRXV4j43/20171027-165414.jpg"><p>35</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rpNzsVwL/20171027-165631.jpg"><p>36</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/44SymFsP/20171027-165647.jpg"><p>37</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8Pf5WBCT/20171027-165802.jpg"><p>38</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FsktGTck/20171027-165830.jpg"><p>39</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nrsWRLsh/20171103-112150.jpg"><p>40</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Rh3Ys03t/20171103-112251.jpg"><p>41</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Y04PnS49/20171103-115436.jpg"><p>42</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Zn9Q7q9p/20171103-115510.jpg"><p>43</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/2SNtGrCL/20171103-115540.jpg"><p>44</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Vk9VHpNJ/20171103-115606.jpg"><p>45</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/k5nprsVW/20171103-115645.jpg"><p>46</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/kXbZWB30/Copia-(2)-di-IMGP1599.jpg"><p>47</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/0Q4WwqVT/DSC00390.jpg"><p>48</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SKyv0dXW/IMG-20171010-WA0013.jpg"><p>49</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3RNfNwFy/IMGP1506.jpg"><p>50</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/mDkpkry8/IMGP1511.jpg"><p>51</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/d1fHyK59/IMGP1573.jpg"><p>52</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sXL6hRnf/IMGP1574.jpg"><p>53</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qqCmcZYM/IMGP1575.jpg"><p>54</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/XXSsskSF/IMGP1576.jpg"><p>55</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Rq5ggL5b/IMGP1597.jpg"><p>56</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Y2Gky2B4/IMGP1598.jpg"><p>57</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/PfghGGd4/IMGP1600.jpg"><p>58</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/dQbvMMqc/IMGP1601.jpg"><p>59</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sD5zsnXr/IMGP1602.jpg"><p>60</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Qds3tp9d/IMGP1633.jpg"><p>61</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/kg9m4x6w/IMGP1635.jpg"><p>62</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Nj4wr5Rw/IMGP1637.jpg"><p>63</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/7LZr1wN6/IMGP1666.jpg"><p>64</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/7LZr1wNT/IMGP1683.jpg"><p>65</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/N0CqpSNC/IMGP1684.jpg"><p>66</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/432kBq8D/IMGP1685.jpg"><p>67</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/NMWhwTvs/IMGP1686.jpg"><p>68</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/6qRk63Br/IMGP1688.jpg"><p>69</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rsWBymqb/IMGP1689.jpg"><p>70</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/x8HwjC0D/IMGP1690.jpg"><p>71</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/28QsPVcb/Immagine-5293.jpg"><p>72</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SN6BwJT8/Immagine-5318.jpg"><p>73</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nLPgv7z4/Immagine-5724.jpg"><p>74</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/85f3w5fQ/Immagine-5775.jpg"><p>75</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/gcRQZxPq/Immagine-5828.jpg"><p>76</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SNfPgHRn/Immagine-5830.jpg"><p>77</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vZ8NkXx2/Immagine-5832.jpg"><p>78</p>


    </div>
    <button class="back-btn" onclick="showHome()">Torna al menu</button>
  </div>

  <div id="pensiline" class="section">
    <h2>Pensiline</h2>
    <div class="gallery">

      <img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/pensiline/realizzazione-pensiline-brescia.jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/pensiline/pensiline-brescia.jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/pensiline/vendita-pensiline-brescia.jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/pensiline/pensiline-bergamo.jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/pensiline/pensiline-bs.jpg"><p>5</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/pensiline/pensiline-2.jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/pensiline/pensilina-new.jpg"><p>7</p>
<img loading="lazy" class="zoom-img" src="https://www.casetteinlegnobrescia.it/pensiline/realizzazione-pensiline.jpg"><p>8</p>

    </div>
    <button class="back-btn" onclick="showHome()">Torna al menu</button>
  </div>

  <div id="chioschi" class="section">
    <h2>Chioschi</h2>
    <div class="gallery">

     <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/h4Z2zzDb/20141014-112546.jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qBD1hhJj/20141026-100917.jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/pVcshhWB/20141205-160002.jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/G3gX88Lp/20141205-160025.jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/tgbkQFkQ/20150322-163425.jpg"><p>5</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/QMqbXVYL/20150322-163509.jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/tgbkQFkp/20150514-200240.jpg"><p>7</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bvPgc1gY/20150514-200428.jpg"><p>8</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Jn4QtmSN/20150525-161917.jpg"><p>9</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Jn65kvLW/20160309-151152.jpg"><p>10</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Y0vffRrt/20160309-151724.jpg"><p>11</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/T1Kqq0d2/20160517-121016.jpg"><p>12</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/hvXbbsDx/20160517-121038.jpg"><p>13</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/kGLNjSDC/20160518-193103.jpg"><p>14</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8zRdHjS3/20160531-191950.jpg"><p>15</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/T3Vj9p6F/20160531-192007.jpg"><p>16</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/wB9Xbgx9/20160710-093457.jpg"><p>17</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vmGrSb8D/20160710-093517.jpg"><p>18</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/25T4sM3x/20160710-093536.jpg"><p>19</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qRR84wC8/20160710-093602.jpg"><p>20</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Y9sQ9F1T/20160710-093637.jpg"><p>21</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/W3H03ZGT/20161103-162021.jpg"><p>22</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Y0LYmSRG/20161103-162038.jpg"><p>23</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/d3ZrT06m/20161108-141702.jpg"><p>24</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/mZP5SN6C/20170505-190528.jpg"><p>25</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qBWZDh9Q/20170505-190603.jpg"><p>26</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/RC2bp6kF/20170505-190625.jpg"><p>27</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rFWZByTz/20170505-190722.jpg"><p>28</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nhGRLdM6/20170505-190752.jpg"><p>29</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/QdJ4M6HM/20170505-190832.jpg"><p>30</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/tgRrnhxm/20170609-152733.jpg"><p>31</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/HLS6wVwF/20170616-170147.jpg"><p>32</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/V6dDDm4C/20170616-170251.jpg"><p>33</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/k4zwHzhT/20170616-170318.jpg"><p>34</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/v8x0n8ct/20170616-170440.jpg"><p>35</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vHR3tRnY/20170616-170516.jpg"><p>36</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Dyq5CCQr/20180208-120535.jpg"><p>37</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/K8xfCnJh/20180405-131109.jpg"><p>38</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/HkzzmVhV/20180405-131218.jpg"><p>39</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Dzzgwn9r/20180405-131233.jpg"><p>40</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/7LQNCj4W/20180524-131048.jpg"><p>41</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/mDzy7V2Q/20180524-131137.jpg"><p>42</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Y0QNs9Wy/20180529-114840.jpg"><p>43</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Bb25V6FX/20180615-130347.jpg"><p>44</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/CM841v2S/20180615-130409.jpg"><p>45</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Gh1xsF0B/20180615-130445.jpg"><p>46</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/c4MM7vZM/20180719-232006.jpg"><p>47</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/MKbb0nxN/20180719-232150.jpg"><p>48</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/wTcc51HS/IMGP1389.jpg"><p>49</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qMXXcN4f/IMGP1428.jpg"><p>50</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sgjPT3Dn/IMGP1430.jpg"><p>51</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/XYjKsn7t/IMGP1434.jpg"><p>52</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SxSLgmxF/IMGP1468.jpg"><p>53</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vZY70GZM/IMGP1469.jpg"><p>54</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/76xK7SJf/IMGP1471.jpg"><p>55</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/6q851y1C/Whats-App-Image-2026-01-22-at-08-31-23.jpg"><p>56</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/0QWyfpnH/Whats-App-Image-2026-01-22-at-08-31-23-(1).jpg"><p>57</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/1X85YfYV/Whats-App-Image-2026-01-22-at-08-31-23-(2).jpg"><p>58</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/2y18XVXZ/Whats-App-Image-2026-01-22-at-08-31-23-(3).jpg"><p>59</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/5yXNk6kB/Whats-App-Image-2026-01-22-at-08-31-24.jpg"><p>60</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Kj1vsRsS/Whats-App-Image-2026-01-22-at-08-31-24-(1).jpg"><p>61</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/054NK0bf/Whats-App-Image-2026-01-22-at-08-31-25.jpg"><p>62</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/DfNz4P8W/Whats-App-Image-2026-01-22-at-08-31-25-(1).jpg"><p>63</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/pVSd5Jp5/Whats-App-Image-2026-01-22-at-08-31-25-(2).jpg"><p>64</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/zv4Xm89w/Whats-App-Image-2026-01-22-at-08-31-25-(3).jpg"><p>65</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sx5DRtsf/Whats-App-Image-2026-01-22-at-08-33-31.jpg"><p>66</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/L5j6Mr2X/Whats-App-Image-2026-01-22-at-08-33-31-(1).jpg"><p>67</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/HWML575b/Whats-App-Image-2026-01-22-at-08-33-32.jpg"><p>68</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sfW2SZS9/Whats-App-Image-2026-01-22-at-08-33-33.jpg"><p>69</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Kz6vwZXg/Whats-App-Image-2026-01-22-at-08-33-33-(1).jpg"><p>70</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ZRGK2Tkg/Whats-App-Image-2026-01-22-at-08-33-33-(2).jpg"><p>71</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FRMs89tB/Whats-App-Image-2026-01-22-at-08-33-34.jpg"><p>72</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bJ7NWzXK/Whats-App-Image-2026-01-22-at-08-33-34-(1).jpg"><p>73</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/gJCkQY9Q/Whats-App-Image-2026-01-22-at-08-33-34-(2).jpg"><p>74</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/MH1K8hxr/Whats-App-Image-2026-01-22-at-08-33-35.jpg"><p>75</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Y0QqwJMc/Whats-App-Image-2026-01-22-at-08-33-35-(1).jpg"><p>76</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/0j72qLPx/Whats-App-Image-2026-01-22-at-08-33-35-(2).jpg"><p>77</p>


    </div>
    <button class="back-btn" onclick="showHome()">Torna al menu</button>
  </div>

  <div id="case-mobili" class="section">
    <h2>Case mobili</h2>
    <div class="gallery">

      <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/NGDkmhp9/20130105-132223.jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/TYHjNV8Y/20130105-132348.jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/gkBytV9d/20130105-132416.jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vHS72rRT/20130105-132607.jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/X7DK1fMC/20130105-132926.jpg"><p>5</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/hGV9GNXm/20130105-133016.jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/gJd3L4hR/20130110-144909.jpg"><p>7</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/NMYR2bXr/20130110-145004.jpg"><p>8</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/pTxK5kjs/20130110-145131.jpg"><p>9</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ZRcp83Fh/20130110-160923.jpg"><p>10</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/4yxtBdBt/20130110-160950.jpg"><p>11</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Wz1rX3X7/20130110-161047.jpg"><p>12</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/J0YXgL2q/20130214-155505(1).jpg"><p>13</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/NFCXVczN/20130214-155724(1).jpg"><p>14</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bYm1dxwv/20130214-155742(1).jpg"><p>15</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/v805DrZt/20130501-114716(1).jpg"><p>16</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nc57Gn7h/20130501-114922.jpg"><p>17</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/mrWHKVmL/20130629-113832(1).jpg"><p>18</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/5t5CJvrj/20130629-113916(1).jpg"><p>19</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/50xF2ycw/20130629-113944(1).jpg"><p>20</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rm8tws6P/20130629-114035(1).jpg"><p>21</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SsDY24qv/20130629-114129(1).jpg"><p>22</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/wMMyDrj5/20130629-120010(1).jpg"><p>23</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/15gVtbTt/20130629-120028(1).jpg"><p>24</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/pXghnqbp/20130629-120059(1).jpg"><p>25</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/P5YLbYTZ/20130629-120128(1).jpg"><p>26</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/kgKVNKqY/20130630-142624(1).jpg"><p>27</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/N0tKdF0c/20130630-142648(1).jpg"><p>28</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/1zS8vXz6/20130630-142739(1).jpg"><p>29</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/W47hCVD9/20130630-142922(1).jpg"><p>30</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sXDvRLSw/20130630-143044(1).jpg"><p>31</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sXDvRLS8/20130709-165423(1).jpg"><p>32</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vT4T4603/20130720-093640.jpg"><p>33</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/WpytQX4S/20130817-092039.jpg"><p>34</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/xjZqWtCY/20130817-092257.jpg"><p>35</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3JDW7m4H/20130817-092307.jpg"><p>36</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/m2FhRCzg/20130819-194007.jpg"><p>37</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/W1Lz4zgr/20130820-081850.jpg"><p>38</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/y84xNxc5/20130909-132400.jpg"><p>39</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/x1vCNQPD/20131006-115901.jpg"><p>40</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/KYmYnW9M/20131006-115936.jpg"><p>41</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/yNn8nT5f/20131006-120000.jpg"><p>42</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/LXX6W1Kc/20131006-120103.jpg"><p>43</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Y99qPWBM/20131006-120329.jpg"><p>44</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/tTMCG49g/20131006-122108.jpg"><p>45</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qq6BJH7X/20131006-122308.jpg"><p>46</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/J0H7rCn8/20131006-122536.jpg"><p>47</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qgfJgDhN/20131122-151313.jpg"><p>48</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/HWrbcJc0/20131122-151341.jpg"><p>49</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/CM9kjFb5/20131122-151355.jpg"><p>50</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Vs2njYXn/20131202-150105.jpg"><p>51</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/RZLt5Ky6/20131202-150150.jpg"><p>52</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Vk8tVDGk/20131206-153154.jpg"><p>53</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/PqfwtNnW/20131206-153218.jpg"><p>54</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/k5MbnDPL/20131206-153233.jpg"><p>55</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ydk3Z5d8/20131206-155001.jpg"><p>56</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/L5Pqy1j6/20131208-090850.jpg"><p>57</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/D0GWCX1q/20131208-095926.jpg"><p>58</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Vs0bs3pT/20140121-151127.jpg"><p>59</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/T25W2ZBM/20140121-151401.jpg"><p>60</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ZYvyY1Xb/20140121-153508.jpg"><p>61</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/KvX310yj/20140121-153635.jpg"><p>62</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/RVc6KwMc/20140121-153752.jpg"><p>63</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bwpGTdJW/20140129-151652.jpg"><p>64</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/9QC4pz0W/20140129-151847.jpg"><p>65</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/x1nkRq8z/20140129-151926.jpg"><p>66</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/GmK4SrTy/20140129-152125.jpg"><p>67</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nLwCpkk9/20140129-152413.jpg"><p>68</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Y950mCZ5/20140129-152441.jpg"><p>69</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/RFkhnZ2z/20140129-152620.jpg"><p>70</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/xCw8b1B9/20140129-152917.jpg"><p>71</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/C5b1CVVF/20140129-153406.jpg"><p>72</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/6qC3VNNf/20140129-153720.jpg"><p>73</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/1RFf1DN8/20140129-153918.jpg"><p>74</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/J4Wtrtbh/20140129-153956.jpg"><p>75</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/4NTnfnzY/20140129-154118.jpg"><p>76</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/xTSqfqK3/20140129-154312.jpg"><p>77</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sgjXW8HY/20140129-154407.jpg"><p>78</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/VkKNWR2H/20140129-154504.jpg"><p>79</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/jSMj4XB8/20140129-154953.jpg"><p>80</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8zZCmHxY/20140129-155014.jpg"><p>81</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Jhg49hrR/20140129-155106.jpg"><p>82</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fbFT6bzS/20140129-155225.jpg"><p>83</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/KzMvFyjC/20140129-155921.jpg"><p>84</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/gJZkdPjC/20140129-160310.jpg"><p>85</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SRbQxtY3/20140129-160912.jpg"><p>86</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Xq6NYDy0/20140129-161003.jpg"><p>87</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Bb5SLcxL/20140129-161310.jpg"><p>88</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/NGRfzYWy/20140129-162410.jpg"><p>89</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/mZ725R0B/20140129-162425.jpg"><p>90</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rFcF63k1/20140129-162538.jpg"><p>91</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/wTHTKZpr/20140129-162907.jpg"><p>92</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/sDcf3mj0/20140129-163026.jpg"><p>93</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/3xx8NGWC/20140129-163233.jpg"><p>94</p>
 <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/g22zjhr8/20140129-163648.jpg"><p>95</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/bwVztv27/20140129-163704.jpg"><p>96</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/0yX8wNws/20140129-164132.jpg"><p>97</p> 
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8CFTBVRs/20140129-164216.jpg"><p>98</p>

    </div>
    <button class="back-btn" onclick="showHome()">Torna al menu</button>
  </div>

  <div id="soluzioni-industriali" class="section">
    <h2>Soluzioni industriali</h2>
    <div class="gallery">

      <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/L8RQRkCX/20130701-141641(1).jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/yNpLFMVX/20130704-092333(1).jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rpwhRVLG/20130704-092453(1).jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/q7D18Pk2/20130708-152328(1).jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8CXZh21m/20130708-152939(1).jpg"><p>5</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/4yVwRnzC/20130708-153014(1).jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/d3rncD8P/20130708-153114(1).jpg"><p>7</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/mkCVWh7q/20130709-120831(1).jpg"><p>8</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/L41x1QGL/20130717-100127(1).jpg"><p>9</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/FsXDgg4t/20130724-074159.jpg"><p>10</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/TYvCqq6T/20130724-074252.jpg"><p>11</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/hPRpbbBg/20130801-091040.jpg"><p>12</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/RV1GP6Sz/20130801-091149.jpg"><p>13</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/jSZcbpJt/20130801-091237.jpg"><p>14</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/JzPxLfB4/20130801-091332.jpg"><p>15</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qvjwTPC7/20130801-091403.jpg"><p>16</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/QMCbxfpN/20130823-151502(1).jpg"><p>17</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/LXZ3jhQp/20130823-151515(1).jpg"><p>18</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/85rmLsXC/20130823-151537(1).jpg"><p>19</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rsXCjc7m/20130823-151606.jpg"><p>20</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Y06NyZwn/20130823-151617(1).jpg"><p>21</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/dQr91kTg/20130823-151639(1).jpg"><p>22</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Yqxf65RM/20130823-151659.jpg"><p>23</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qvbsY29d/20130823-151718(1).jpg"><p>24</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/nLX4tCJj/20130823-151745(1).jpg"><p>25</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/9fsGXCmL/20130823-151927(1).jpg"><p>26</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/W3r0hCtR/20130823-152428(1).jpg"><p>27</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/kGmK8stp/20140526-141119.jpg"><p>28</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/c1RQWpVk/20140526-183943.jpg"><p>29</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/15yD3WSN/20140609-150825.jpg"><p>30</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/BQNHLxZv/20140609-151009.jpg"><p>31</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/GhzG8k3K/20140609-151454.jpg"><p>32</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/vHXfgW82/20140802-192154-Copia.jpg"><p>33</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Z5MNj4dm/20140802-192329-Copia.jpg"><p>34</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/ht5mMcdQ/20140802-192743.jpg"><p>35</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/rm6rXjgF/20140918-130113.jpg"><p>36</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/NMhHqDb5/20140918-130222.jpg"><p>37</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/D06JGThh/20140918-130342.jpg"><p>38</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/C57B8g05/20140918-130649.jpg"><p>39</p>

<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/BQZ10X5x/20160502-101840.jpg"><p>41</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/W1hFdCf9/20160502-101931.jpg"><p>42</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/jd8ndtvg/CASETTA-MONICA-GHIDINI-03.jpg"><p>43</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/Z5CBW2Dg/foto-edilgarde1-022.jpg"><p>44</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/T3pLKFHz/foto-edilgarde1-040.jpg"><p>45</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/mgJcCjvF/IMGP0986.jpg"><p>46</p>


    </div>
    <button class="back-btn" onclick="showHome()">Torna al menu</button>
  </div>

  <div id="case-abitabili" class="section">
    <h2>Case abitabili</h2>
    <div class="gallery">

      <img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fy3VjZkq/Whats-App-Image-2026-01-14-at-16-32-28.jpg"><p>1</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/1t7gq4R6/Whats-App-Image-2026-01-14-at-16-32-28-(1).jpg"><p>2</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SRXn7qjt/Whats-App-Image-2026-01-14-at-16-33-47.jpg"><p>3</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/gjwxqdnk/Whats-App-Image-2026-01-14-at-16-33-49.jpg"><p>4</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/gjfng5ZX/Whats-App-Image-2026-01-14-at-16-33-51.jpg"><p>5</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/hvJXbgfD/Whats-App-Image-2026-01-14-at-16-33-51-(1).jpg"><p>6</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/qqtNX0zt/Whats-App-Image-2026-01-14-at-16-33-52.jpg"><p>7</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/PJBPScw2/Whats-App-Image-2026-01-14-at-16-33-53.jpg"><p>8</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/kGkBTZbS/Whats-App-Image-2026-01-14-at-16-33-53-(1).jpg"><p>9</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/SQ52QXvR/Whats-App-Image-2026-01-14-at-16-33-54.jpg"><p>10</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/hvHf2wdM/Whats-App-Image-2026-01-14-at-16-33-54-(1).jpg"><p>11</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/MZ4MZcF6/Whats-App-Image-2026-01-14-at-16-33-54-(2).jpg"><p>12</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/PrwLCtg8/Whats-App-Image-2026-01-14-at-16-33-55.jpg"><p>13</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/VsTrsSV0/Whats-App-Image-2026-01-14-at-16-33-55-(1).jpg"><p>14</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/xj7Jjk4b/Whats-App-Image-2026-01-14-at-16-33-55-(2).jpg"><p>15</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/8k3JkF0L/Whats-App-Image-2026-01-14-at-16-33-55-(3).jpg"><p>16</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/dty7hqb7/Whats-App-Image-2026-01-14-at-16-33-55-(4).jpg"><p>17</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/PrwLCtgR/Whats-App-Image-2026-01-14-at-16-33-56.jpg"><p>18</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/CLqZRF38/Whats-App-Image-2026-01-14-at-16-33-56-(1).jpg"><p>19</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/fT93VwGK/Whats-App-Image-2026-01-14-at-16-33-56-(2).jpg"><p>20</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/hPdJXSk2/Whats-App-Image-2026-01-14-at-16-33-56-(3).jpg"><p>21</p>
<img loading="lazy" class="zoom-img" src="https://i.postimg.cc/L8FJfcSv/Whats-App-Image-2026-01-14-at-16-33-57.jpg"><p>22</p>


    </div>
    <button class="back-btn" onclick="showHome()">Torna al menu</button>
  </div>

</div>

<!-- POPUP ZOOM -->
<div id="zoom-popup">
  <img id="zoom-img" loading="lazy" class="zoom-img" src="">
</div>

<script>
  function openSection(id) {
    document.getElementById("home").style.display = "none";
    document.querySelectorAll(".section").forEach(s => s.style.display = "none");
    document.getElementById(id).style.display = "block";
  }

  function openSub(id) {
    document.querySelectorAll(".section").forEach(s => s.style.display = "none");
    document.getElementById(id).style.display = "block";
  }

  function showHome() {
    document.querySelectorAll(".section").forEach(s => s.style.display = "none");
    document.getElementById("home").style.display = "block";  
  }

  const popup = document.getElementById("zoom-popup");
  const popupImg = document.getElementById("zoom-img");

  let scale = 1;

  document.querySelectorAll('.gallery img').forEach(img => {
    img.addEventListener('click', () => {
      popupImg.src = img.src;
      popup.style.display = "flex";
      scale = 1;
      popupImg.style.transform = "scale(1)";
    });
  });

  // Zoom con rotella del mouse (solo quando l'immagine è aperta)
  popupImg.addEventListener("wheel", e => {
    e.preventDefault();
    // deltaY positivo = rotella giù (zooma out), negativo = rotella su (zooma in)
    scale += e.deltaY * -0.001;
    scale = Math.min(Math.max(0.5, scale), 4); // limite 0.5x - 4x
    popupImg.style.transform = `scale(${scale})`;
  });

  // chiudi solo cliccando sul backdrop (non sulla stessa immagine)
  popup.addEventListener('click', (e) => {
    if (e.target === popup) {
      popup.style.display = "none";
      popupImg.style.transform = "scale(1)";
      popupImg.src = "";
    }
  });

</script>

