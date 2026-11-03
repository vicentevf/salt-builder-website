# Salt Builders website

Single-page site for Salt Builders (new builds, renovations, alterations and outdoor areas).

- `index.html` is the whole site (HTML, CSS and JavaScript). The logo, director photos and hero photo are embedded in it.
- `images/` holds the 9 project photos shown in the "Our projects" gallery (`project-1.jpg` ... `project-9.jpg`).
- Only external requests: Google Fonts (Inclusive Sans) and the contact form service (formsubmit.co).
- Hosting: GitHub Pages (Settings > Pages > Deploy from a branch > `main` / root).

## Contact form (one-time activation)
The contact form sends messages to **enquire@saltbuilders.co.nz** through FormSubmit (free, no account).

1. Open the LIVE site (not the file on a computer) and send a test message through the form.
2. FormSubmit emails an activation link to enquire@saltbuilders.co.nz (check Spam too). Click it. The test message is delivered after activation, and every later message arrives directly.
3. Recommended: once activated, FormSubmit provides a random-string address. Use it so the real email is not readable in the page source. In `index.html` change ONLY these two places:
   - the form tag: `action="https://formsubmit.co/<random-string>"`
   - the script: `FORM_ENDPOINT='https://formsubmit.co/ajax/<random-string>'`
   Do NOT change `MAIL='enquire@saltbuilders.co.nz'`: it is the fallback shown when sending fails and must stay the real email address.

If sending fails, the form shows a "Details:" line with the reason, plus a link that opens the visitor's email app addressed to the business.

## Changing a project photo
Replace the file in `images/` with a new JPG using the same name. The captions are in `index.html`, inside the `<figure class="slot">` blocks.
