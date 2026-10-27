# Typeo SEO and Google Search Console setup

Production site: https://typing-speedtest.pages.dev/
Sitemap: https://typing-speedtest.pages.dev/sitemap.xml

## Google Search Console — URL-prefix property

1. Open https://search.google.com/search-console/ and sign in.
2. Choose **Add property** → **URL prefix**.
3. Enter exactly `https://typing-speedtest.pages.dev/`.
4. Choose **HTML tag** verification. Copy the complete meta tag Google provides.
5. Paste that tag inside the `<head>` of `index.html`, then deploy the updated site.
6. Open the live homepage, view its page source, and confirm the verification meta tag is present.
7. Return to Search Console and click **Verify**.
8. In Search Console, open **Sitemaps**, enter `sitemap.xml`, and submit.
9. Use **URL inspection** for the homepage and important pages, then choose **Request indexing** if available.

## Important
- Search Console verification is account-specific. Use the exact token Google shows; no token has been fabricated.
- `sitemap.xml` is the XML sitemap at the site root. Do not submit `seo_sitemap.md` as a sitemap.
- `typo.html` duplicates the homepage and is redirected to `/` by Cloudflare Pages `_redirects`.
- Sitemap submission is a discovery hint, not a guarantee of indexing or ranking.
- The contact form uses FormSubmit. Replace `YOUR_EMAIL_HERE` in `contact_us_page.html` with your receiving email, deploy, submit a test message, and confirm the FormSubmit email.
