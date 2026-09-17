<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Vidora - منصة احترافية لإدارة روابط الفيديوهات وYouTube Shorts.">
  <title>Vidora | منصة الفيديو</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link
    href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;800;900&display=swap"
    rel="stylesheet"
  >

  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
  >

  <style>
    :root {
      --bg: #f8fafc;
      --card: #fff;
      --blue: #2563eb;
      --blue-dark: #1d4ed8;
      --blue-light: #eff6ff;
      --red: #ff0000;
      --green: #10b981;
      --text: #0f172a;
      --muted: #64748b;
      --border: #e2e8f0;
      --shadow: 0 10px 25px -5px rgba(37, 99, 235, .10);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      -webkit-tap-highlight-color: transparent;
    }

    body {
      font-family: "Cairo", sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
      line-height: 1.6;
    }

    .header {
      position: sticky;
      top: 0;
      z-index: 100;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 18px;
      background: #fff;
      border-bottom: 1px solid var(--border);
    }

    .logo {
      text-decoration: none;
      color: var(--text);
      font-size: 24px;
      font-weight: 900;
    }

    .logo i,
    .logo span {
      color: var(--blue);
    }

    .badges {
      display: flex;
      gap: 6px;
    }

    .badge {
      padding: 5px 9px;
      border-radius: 20px;
      font-size: 10px;
      font-weight: 800;
    }

    .youtube {
      color: var(--red);
      background: #fef2f2;
      border: 1px solid #fecaca;
    }

    .shorts {
      color: var(--blue);
      background: var(--blue-light);
      border: 1px solid #bfdbfe;
    }

    .container {
      max-width: 520px;
      margin: auto;
      padding: 28px 16px;
    }

    .hero {
      text-align: center;
      margin-bottom: 24px;
    }

    .hero h1 {
      font-size: 25px;
      font-weight: 900;
      line-height: 1.35;
    }

    .hero h1 span {
      color: var(--blue);
    }

    .hero p {
      margin-top: 7px;
      font-size: 13px;
      color: var(--muted);
      font-weight: 600;
    }

    .downloader {
      background: var(--card);
      border: 2px solid var(--blue);
      border-radius: 24px;
      padding: 16px;
      box-shadow: var(--shadow);
    }

    .input-box {
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 10px 12px;
      background: #f1f5f9;
      border: 1px solid var(--border);
      border-radius: 15px;
    }

    .input-box i {
      color: var(--red);
      font-size: 21px;
    }

    .input-box input {
      width: 100%;
      border: 0;
      outline: 0;
      background: transparent;
      font-family: inherit;
      font-size: 14px;
      font-weight: 600;
    }

    .buttons {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 10px;
      margin-top: 12px;
    }

    button {
      border: 0;
      cursor: pointer;
      font-family: inherit;
      font-weight: 800;
      border-radius: 11px;
      padding: 12px;
    }

    .paste {
      color: var(--blue);
      background: var(--blue-light);
      border: 1px solid #bfdbfe;
    }

    .process {
      color: white;
      background: var(--blue);
    }

    .process:active,
    .paste:active,
    .download:active {
      transform: scale(.98);
    }

    .preview {
      display: none;
      margin-top: 20px;
      background: #fff;
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 16px;
    }

    .video-header {
      display: flex;
      gap: 12px;
      align-items: center;
    }

    .thumbnail {
      width: 90px;
      height: 90px;
      border-radius: 10px;
      background: #dbeafe;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      flex-shrink: 0;
    }

    .thumbnail img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: none;
    }

    .thumbnail i {
      color: var(--blue);
      font-size: 28px;
    }

    .video-info {
      overflow: hidden;
    }

    .video-title {
      font-size: 14px;
      font-weight: 800;
    }

    .video-info p {
      margin-top: 5px;
      font-size: 11px;
      color: var(--muted);
    }

    .format {
      width: 100%;
      margin-top: 15px;
      padding: 12px;
      border: 1px solid var(--border);
      border-radius: 10px;
      background: #f8fafc;
      font-family: inherit;
      font-weight: 700;
    }

    .download {
      width: 100%;
      margin-top: 10px;
      color: white;
      background: var(--green);
    }

    .tip {
      margin-top: 20px;
      padding: 14px;
      display: flex;
      gap: 10px;
      background: var(--blue-light);
      border: 1px dashed #bfdbfe;
      border-radius: 15px;
      font-size: 12px;
      color: #1e3a8a;
      font-weight: 600;
    }

    .tip i {
      color: var(--blue);
      margin-top: 3px;
    }

    .section {
      margin-top: 40px;
      padding-top: 30px;
      border-top: 2px solid var(--border);
    }

    .heading {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 16px;
      font-size: 18px;
      font-weight: 900;
    }

    .heading i {
      color: var(--blue);
    }

    .steps {
      display: grid;
      gap: 12px;
    }

    .step,
    .feature,
    .article,
    .faq {
      background: white;
      border: 1px solid var(--border);
      border-radius: 14px;
    }

    .step {
      display: flex;
      align-items: center;
      gap: 12px;
      padding: 14px;
    }

    .number {
      width: 32px;
      height: 32px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      color: white;
      background: var(--blue);
      border-radius: 50%;
      font-weight: 900;
    }

    .step h4,
    .feature h4 {
      font-size: 13px;
    }

    .step p,
    .feature p,
    .article p,
    .faq-answer {
      color: var(--muted);
      font-size: 12px;
    }

    .features {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 12px;
    }

    .feature {
      text-align: center;
      padding: 15px;
    }

    .feature-icon {
      width: 40px;
      height: 40px;
      margin: auto auto 8px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--blue);
      background: var(--blue-light);
      border-radius: 10px;
    }

    .article {
      padding: 18px;
      margin-bottom: 15px;
    }

    .article h3 {
      margin-bottom: 8px;
      color: var(--blue);
      font-size: 15px;
    }

    .article p {
      line-height: 1.8;
    }

    .faq {
      margin-bottom: 10px;
      overflow: hidden;
    }

    .faq-question {
      padding: 14px;
      font-size: 13px;
      font-weight: 800;
      cursor: pointer;
    }

    .faq-answer {
      display: none;
      padding: 0 14px 14px;
      line-height: 1.7;
    }

    .faq.open .faq-answer {
      display: block;
    }

    footer {
      margin-top: 40px;
      padding: 25px 16px;
      text-align: center;
      background: white;
      border-top: 1px solid var(--border);
    }

    .footer-links {
      display: flex;
      justify-content: center;
      gap: 18px;
      margin-bottom: 10px;
    }

    .footer-links a {
      color: var(--muted);
      text-decoration: none;
      font-size: 12px;
    }

    .copyright {
      color: #94a3b8;
      font-size: 11px;
    }

    @media (max-width: 380px) {
      .badge {
        display: none;
      }

      .hero h1 {
        font-size: 22px;
      }
    }
  </style>
</head>

<body>

<header class="header">

  <a href="#" class="logo">
    <i class="fa-solid fa-circle-down"></i>
    Vid<span>ora</span>
  </a>

  <div class="badges">

    <div class="badge youtube">
      <i class="fa-brands fa-youtube"></i>
      YouTube
    </div>

    <div class="badge shorts">
      <i class="fa-solid fa-bolt"></i>
      Shorts
    </div>

  </div>

</header>

<main class="container">

  <section class="hero">

    <h1>
      محمل فيديوهات و <span>Shorts</span> يوتيوب
    </h1>

    <p>
      واجهة Vidora الاحترافية — سريعة ومناسبة للهاتف
    </p>

  </section>

  <section class="downloader">

    <div class="input-box">

      <i class="fa-brands fa-youtube"></i>

      <input
        type="url"
        id="videoUrlInput"
        placeholder="ضع رابط الفيديو أو Shorts هنا..."
        autocomplete="off"
      >

    </div>

    <div class="buttons">

      <button
        type="button"
        class="paste"
        onclick="handlePaste()"
      >
        <i class="fa-regular fa-clipboard"></i>
        لصق
      </button>

      <button
        type="button"
        class="process"
        onclick="processVideo()"
      >
        <i class="fa-solid fa-download"></i>
        تحميل الآن
      </button>

    </div>

  </section>

  <section class="preview" id="preview">

    <div class="video-header">

      <div class="thumbnail">

        <img
          id="thumbnail"
          alt="Video thumbnail"
        >

        <i
          id="playIcon"
          class="fa-solid fa-play"
        ></i>

      </div>

      <div class="video-info">

        <div
          class="video-title"
          id="videoTitle"
        >
          فيديو YouTube
        </div>

        <p id="videoType">
          تم التعرف على الرابط
        </p>

      </div>

    </div>

    <select class="format" id="format">

      <option value="mp4-1080">
        MP4 1080p Full HD
      </option>

      <option value="mp4-720" selected>
        MP4 720p HD
      </option>

      <option value="mp4-480">
        MP4 480p
      </option>

      <option value="mp4-360">
        MP4 360p
      </option>

      <option value="mp3">
        MP3
      </option>

    </select>

    <button
      type="button"
      class="download"
      onclick="startDownload()"
    >
      <i class="fa-solid fa-arrow-down"></i>
      تنزيل
    </button>

  </section>

  <div class="tip">

    <i class="fa-solid fa-lightbulb"></i>

    <p>
      <b>طريقة الاستخدام:</b>
      انسخ رابط الفيديو من YouTube، ثم اضغط «لصق» وأرسل الرابط.
    </p>

  </div>

  <section class="section">

    <h2 class="heading">
      <i class="fa-solid fa-list-check"></i>
      خطوات الاستخدام
    </h2>

    <div class="steps">

      <div class="step">

        <div class="number">1</div>

        <div>
          <h4>انسخ الرابط</h4>
          <p>انسخ رابط الفيديو أو Shorts.</p>
        </div>

      </div>

      <div class="step">

        <div class="number">2</div>

        <div>
          <h4>ألصق الرابط</h4>
          <p>ضع الرابط في مربع Vidora.</p>
        </div>

      </div>

      <div class="step">

        <div class="number">3</div>

        <div>
          <h4>اختر الصيغة</h4>
          <p>اختر الصيغة المناسبة عند توفر الخدمة.</p>
        </div>

      </div>

    </div>

    <h2
      class="heading"
      style="margin-top:35px;"
    >
      <i class="fa-solid fa-star"></i>
      مميزات Vidora
    </h2>

    <div class="features">

      <div class="feature">

        <div class="feature-icon">
          <i class="fa-solid fa-bolt"></i>
        </div>

        <h4>سرعة</h4>
        <p>واجهة خفيفة وسريعة.</p>

      </div>

      <div class="feature">

        <div class="feature-icon">
          <i class="fa-solid fa-mobile-screen"></i>
        </div>

        <h4>هاتف</h4>
        <p>تصميم مناسب للجوال.</p>

      </div>

      <div class="feature">

        <div class="feature-icon">
          <i class="fa-solid fa-link"></i>
        </div>

        <h4>سهولة</h4>
        <p>واجهة بسيطة وواضحة.</p>

      </div>

      <div class="feature">

        <div class="feature-icon">
          <i class="fa-solid fa-shield-halved"></i>
        </div>

        <h4>واجهة آمنة</h4>
        <p>بدون بيانات شخصية.</p>

      </div>

    </div>

    <h2
      class="heading"
      style="margin-top:35px;"
    >
      <i class="fa-solid fa-book-open"></i>
      دليل Vidora
    </h2>

    <article class="article">

      <h3>ما هو YouTube Shorts؟</h3>

      <p>
        YouTube Shorts هو نظام الفيديوهات القصيرة في YouTube.
        صُممت Vidora بواجهة مناسبة للتعامل مع روابط الفيديوهات القصيرة
        بطريقة بسيطة على الهاتف.
      </p>

    </article>

    <article class="article">

      <h3>Vidora على الهاتف</h3>

      <p>
        تم تصميم الواجهة بأسلوب Mobile First لتكون سهلة الاستخدام
        على الهواتف والشاشات الصغيرة.
      </p>

    </article>

    <h2 class="heading">

      <i class="fa-solid fa-circle-question"></i>
      الأسئلة الشائعة

    </h2>

    <div class="faq">

      <div
        class="faq-question"
        onclick="toggleFaq(this)"
      >
        هل Vidora مجانية؟
      </div>

      <div class="faq-answer">
        الواجهة مجانية، أما خدمات المعالجة والتنزيل فسيتم ربطها
        بالـBackend في المرحلة القادمة.
      </div>

    </div>

    <div class="faq">

      <div
        class="faq-question"
        onclick="toggleFaq(this)"
      >
        هل تعمل على الهاتف؟
      </div>

      <div class="faq-answer">
        نعم، الواجهة مصممة أساسًا للهواتف ويمكن استخدامها أيضًا على الكمبيوتر.
      </div>

    </div>

    <div class="faq">

      <div
        class="faq-question"
        onclick="toggleFaq(this)"
      >
        هل تم ربط Backend؟
      </div>

      <div class="faq-answer">
        ليس بعد. سيتم إضافة Backend في المرحلة التالية.
      </div>

    </div>

  </section>

</main>

<footer>

  <div class="footer-links">

    <a href="#">الرئيسية</a>
    <a href="#">الخصوصية</a>
    <a href="#">شروط الاستخدام</a>

  </div>

  <div class="copyright">
    © 2026 Vidora — جميع الحقوق محفوظة
  </div>

</footer>

<script>

  function getYouTubeId(url) {

    try {

      const parsed = new URL(url);

      if (parsed.hostname.includes("youtu.be")) {

        return parsed.pathname
          .substring(1)
          .split("/")[0];

      }

      if (parsed.hostname.includes("youtube.com")) {

        if (parsed.pathname === "/watch") {

          return parsed.searchParams.get("v");

        }

        if (parsed.pathname.startsWith("/shorts/")) {

          return parsed.pathname
            .split("/shorts/")[1]
            .split("/")[0];

        }

        if (parsed.pathname.startsWith("/embed/")) {

          return parsed.pathname
            .split("/embed/")[1]
            .split("/")[0];

        }

      }

      return null;

    } catch {

      return null;

    }

  }


  async function handlePaste() {

    try {

      const text = await navigator.clipboard.readText();

      if (!text) {

        alert("الحافظة فارغة.");

        return;

      }

      document.getElementById("videoUrlInput").value = text;

    } catch {

      alert(
        "لم يتم السماح بالوصول إلى الحافظة. ألصق الرابط يدويًا."
      );

    }

  }


  function processVideo() {

    const input =
      document.getElementById("videoUrlInput");

    const url = input.value.trim();

    if (!url) {

      alert("أدخل رابط YouTube أولاً.");

      return;

    }

    const videoId = getYouTubeId(url);

    if (!videoId) {

      alert("الرابط غير صالح أو غير مدعوم.");

      return;

    }

    const preview =
      document.getElementById("preview");

    const thumbnail =
      document.getElementById("thumbnail");

    const playIcon =
      document.getElementById("playIcon");

    const title =
      document.getElementById("videoTitle");

    const type =
      document.getElementById("videoType");


    thumbnail.src =
      "https://i.ytimg.com/vi/" +
      videoId +
      "/hqdefault.jpg";

    thumbnail.style.display = "block";

    playIcon.style.display = "none";


    if (
      new URL(url).pathname.startsWith("/shorts/")
    ) {

      type.textContent = "YouTube Shorts";

      title.textContent = "YouTube Shorts";

    } else {

      type.textContent = "YouTube Video";

      title.textContent = "YouTube Video";

    }


    preview.style.display = "block";


    preview.scrollIntoView({

      behavior: "smooth",

      block: "center"

    });

  }


  function startDownload() {

    const input =
      document.getElementById("videoUrlInput");

    const url = input.value.trim();


    if (!url) {

      alert("أدخل رابط YouTube أولاً.");

      return;

    }


    const videoId = getYouTubeId(url);


    if (!videoId) {

      alert("الرابط غير صالح أو غير مدعوم.");

      return;

    }


    const format =
      document.getElementById("format").value;


    const formatText =
      document.getElementById("format")
      .options[
        document.getElementById("format").selectedIndex
      ].text;


    alert(
      "تم التعرف على الفيديو بنجاح!\n\n" +
      "الصيغة: " +
      formatText +
      "\n\n" +
      "التنزيل الفعلي سيتم بعد ربط Backend."
    );

  }


  function toggleFaq(element) {

    const faq =
      element.parentElement;

    faq.classList.toggle("open");

  }

</script>

</body>
</html>