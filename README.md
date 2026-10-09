# Export Readiness Assessment: setup for www.gsmsllc.com

Instructions for GT Universe. The assessment is already built, hosted and connected to our CRM. There is nothing to build or wire up: it only needs a page on the site and a button on the homepage.

## 1. New page: www.gsmsllc.com/export-assessment

Create the page with the normal site header, menu and footer. Title it "Free Export Assessment", then paste this into the content area:

```html
<section class="gbed-assess-page">
  <h2>Free Export Assessment</h2>
  <p class="lead2">Is your brand ready to export? Answer 7 quick questions and get an instant readiness read from our trade team.</p>
  <div class="gbed-assess-card">
    <iframe id="gbed-export-quiz"
            src="https://felixvilla-cell.github.io/export-readiness/"
            title="Export Readiness Assessment"
            style="width:100%;border:0;display:block;height:720px;"></iframe>
  </div>
</section>
<script>
  // Resizes the frame to fit each step of the assessment.
  window.addEventListener("message", function (e) {
    if (e.origin !== "https://felixvilla-cell.github.io") return;
    if (e.data && e.data.type === "gbed-export-quiz-height") {
      document.getElementById("gbed-export-quiz").style.height = (e.data.height + 10) + "px";
    }
  });
</script>
```

Add this to the site CSS (css/main.css):

```css
.gbed-assess-page{background:#f5f8fb;padding:46px 16px 60px;}
.gbed-assess-page h2{font-family:"Lato",sans-serif;font-weight:900;color:#024982;text-align:center;margin:0 0 8px;}
.gbed-assess-page p.lead2{font-family:"Lato",sans-serif;text-align:center;color:#5d6b7a;margin:0 auto 26px;max-width:620px;}
.gbed-assess-card{max-width:520px;margin:0 auto;background:#fff;border-radius:10px;box-shadow:0 6px 24px rgba(2,73,130,.10);overflow:hidden;}
```

The assessment already uses the site's blue, the Lato font and the Global logo. When it is embedded it hides its own logo, since the site header already shows it.

## 2. Homepage button

In the homepage hero, right under the sub-title ("by taking a vertical sales approach..."), add:

```html
<a class="gbed-assess-btn" href="/export-assessment">Free Export Assessment</a>
```

and this CSS:

```css
.gbed-assess-btn{display:inline-block;margin-top:26px;background:#ffffff;color:#0061ad;font-family:"Lato",sans-serif;font-weight:700;
 font-size:18px;padding:14px 30px;border-radius:6px;text-decoration:none;box-shadow:0 4px 14px rgba(0,0,0,.18);}
.gbed-assess-btn:hover{background:#e8f2fb;color:#024982;}
```

A link in the main menu or on the Export Sales page is optional and uses the same /export-assessment address.

## Good to know

- Submissions go straight to our CRM. Nothing on the website side handles or stores form data.
- Any change to the questions or wording updates inside the page automatically. The website never needs to be touched again for those.

Questions: Felix Villa.
