# Export Readiness Assessment

A short self-assessment for food and beverage brands: 7 questions, an instant result, and a contact form that goes straight to our sales team.

**Live page:** https://felixvilla-cell.github.io/export-readiness/

## For the website team

The assessment is fully hosted and working. Nothing needs to be built on your side. Pick one of these:

### Option 1: Link to it (simplest)

Add a button or menu item that opens the live page, for example "Free Export Assessment".

### Option 2: Embed it on a page

Paste this where the assessment should appear. The frame resizes itself to fit each step.

```html
<iframe id="gbed-export-quiz"
        src="https://felixvilla-cell.github.io/export-readiness/"
        title="Export Readiness Assessment"
        style="width:100%;max-width:520px;border:0;display:block;margin:0 auto;height:720px;"
        loading="lazy"></iframe>
<script>
  window.addEventListener("message", function (e) {
    if (e.origin !== "https://felixvilla-cell.github.io") return;
    if (e.data && e.data.type === "gbed-export-quiz-height") {
      document.getElementById("gbed-export-quiz").style.height = (e.data.height + 10) + "px";
    }
  });
</script>
```

### Styling

The colors and fonts are placeholders. If you want it to match the site, send us the brand colors, font and logo and we will update the hosted page, so your embed picks up the change with no work on your side.

### Questions

Contact Felix Villa.
