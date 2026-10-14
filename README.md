# EAGLE - CS Official Website

A responsive bilingual (English/Arabic) website for the EAGLE - CS Counter-Strike community. It includes home, news/announcements, player report form, and staff contact sections.

## Included files
- `index.html` — page content, SEO metadata, report form
- `style.css` — responsive black/red military-inspired visual design
- `script.js` — Arabic/English switch, mobile navigation, report submission

## 1. Activate real report delivery (Formspree)

The report form is intentionally not connected until you configure your own endpoint. This avoids sending player reports to an account you do not control.

1. Visit **https://formspree.io/** and create an account.
2. Create a new form and set the destination email to an email address controlled by your server staff.
3. Formspree will provide a form endpoint similar to `https://formspree.io/f/abcdwxyz`.
4. Open `index.html` and find:
   `action="https://formspree.io/f/YOUR_FORM_ID"`
5. Replace `YOUR_FORM_ID` with the actual ID from your Formspree endpoint. Example only:
   `action="https://formspree.io/f/abcdwxyz"`
6. Save and publish the change. Confirm your email address in Formspree if requested.
7. Test a report from the published website and confirm that the staff inbox receives it. Check spam/junk too.

**Important:** the free plan and usage limits may change. Check Formspree's current terms. Do not ask players for passwords or sensitive personal data. Tell staff to handle evidence and contact details carefully. Add spam protection or moderation if the form begins receiving abuse.

## 2. Add your Discord invite

In `index.html`, find:
`https://discord.com/`
Replace it with your own Discord invite or support channel URL. Do not publish a private staff-only link if players should not access it.

## 3. Publish free with GitHub Pages

1. Sign in at https://github.com/.
2. Create a **public** repository named `eagle-cs-website`.
3. Upload `index.html`, `style.css`, `script.js`, and `README.md` to the repository root.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, select **Deploy from a branch**.
6. Choose branch `main` and folder `/(root)`, then Save.
7. Wait for the deployment to complete. Your URL will look like:
   `https://YOUR-USERNAME.github.io/eagle-cs-website/`
8. Open the website on desktop and phone. Test both languages and the report form.

### Before launch
- Replace the canonical URL in `index.html`:
  `https://YOUR-USERNAME.github.io/eagle-cs-website/`
  with your actual GitHub Pages URL.
- Replace the Discord link.
- Configure Formspree.
- Replace sample news with real announcements.
- Do not add a server IP or claim the server is online until you have verified it.

## 4. Google indexing

1. Open https://search.google.com/search-console/.
2. Add a **URL prefix** property with the exact published GitHub Pages URL.
3. Complete one of Google's offered verification methods. Depending on the available method, this may involve adding an HTML verification file to the repository.
4. Use **URL Inspection** for the homepage URL and select **Request indexing**.
5. Check the property again later. Crawling/indexing is not instant and submitting a request does not guarantee a particular ranking.

The site includes a title, description, canonical URL, and basic social metadata. Search ranking depends on many factors; using the name consistently in community profiles and linking to the site can help people find it.

## 5. Editing announcements

Open `index.html`, search for `WELCOME` or `Welcome to EAGLE - CS`, and edit the sample announcement cards. The text shown on the page is currently static, so changing the HTML is the simplest way to publish news on GitHub Pages.

## Limitations

GitHub Pages hosts static files. The report form is received by Formspree after you configure it; the site does not include a private database, staff login, or report dashboard. Never put private API keys or passwords in these public files.
