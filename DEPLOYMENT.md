# Deploying Luyanda Nkosi's Portfolio on Netlify

Site address: https://luyandankosi.netlify.app
(All files already point to this address.)

## What is in the folder
| File | Purpose |
|---|---|
| index.html | The site, with SEO tags, social preview and structured data |
| sitemap.xml, robots.txt | Tell Google/Bing what to index |
| 404.html | Netlify shows this automatically for missing pages |
| _headers | Netlify security and caching rules |
| favicon.svg, favicon-32.png, apple-touch-icon.png, site.webmanifest | Icons |
| assets/ | Social preview image (og-image.png) and icons |
| humans.txt, .well-known/security.txt | Optional credit/contact files |

## Before you upload (2 minutes)
1. Replace the two GitHub links in index.html (search for `href="#"`) with your GitHub profile URL, or delete them.
2. Check the Experience section against your LinkedIn (see the TODO comment in the code).

## Deploy on Netlify
1. Unzip `luyanda-portfolio-netlify.zip` on your computer. You should get a folder containing index.html directly (not a folder inside a folder).
2. Go to https://app.netlify.com and sign up (free) with your email, Google or GitHub.
3. On your dashboard choose **Add new project > Deploy manually**.
4. Drag the unzipped **folder** onto the upload box. Netlify publishes it in a few seconds and gives you a random address like `random-name-123.netlify.app`.
5. Open **Project configuration > Domain management > Options > Edit project name**. Type `luyandankosi` and save. Your site is now at https://luyandankosi.netlify.app.
   - If the name is taken, choose another (e.g. `luyanda-nkosi`). Then update every address in the files to match: open each file in VS Code and use Find and Replace on `luyandankosi.netlify.app` (index.html, sitemap.xml, robots.txt, .well-known/security.txt). Re-upload afterwards.
6. HTTPS is enabled automatically. Visit the address and check that it loads.
7. To update later: **Deploys** tab, then drag the updated folder onto the "Drag and drop" area.

## Test it
- https://luyandankosi.netlify.app/robots.txt and /sitemap.xml open and show your address.
- https://luyandankosi.netlify.app/nothing shows your custom 404 page.
- Share the link on WhatsApp and LinkedIn: the title and preview image should appear. For LinkedIn use linkedin.com/post-inspector to refresh its cache.
- Structured data check: search.google.com/test/rich-results

## Get found on Google and Bing
1. Go to https://search.google.com/search-console and add a **URL prefix** property: `https://luyandankosi.netlify.app/`.
2. Verify it. Easiest method: choose **HTML tag**, copy the `<meta name="google-site-verification" ...>` line into the `<head>` of index.html, re-upload the folder to Netlify, then click Verify.
3. In **Sitemaps**, submit `sitemap.xml`. Then in **URL Inspection**, enter your homepage and click **Request indexing**.
4. Do the same at https://www.bing.com/webmasters (you can import from Search Console).
5. Allow a few days to a few weeks. Searching "Luyanda Nkosi" should find you first.

## Help people find you
- Add the link to your LinkedIn (Contact info and Featured), GitHub profile, CV and email signature.
- Use the name "Luyanda Nkosi" the same way everywhere.
- Add more detail to your projects over time (screenshots, GitHub links, case studies).

## Optional: your own domain later
If you later buy something like luyandankosi.co.za, add it under **Domain management > Add a domain** in Netlify and follow its DNS steps, then replace `https://luyandankosi.netlify.app` with the new address in all files and re-upload.

## Maintenance
- Update `lastmod` in sitemap.xml after major edits.
- security.txt expires 2027-10-15; update the date or delete the file.
