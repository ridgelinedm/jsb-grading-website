# JSB Grading LLC — Website

A minimalist, multi-page static website for JSB Grading LLC, a land grading
company serving Greenville County and Upstate South Carolina.

Built with plain HTML, CSS, and a few lines of JavaScript — no frameworks, no
build step. Ready to host anywhere, including GitHub Pages.

## Structure

```
index.html                 # homepage
about.html                 # about Jeff / the company
services.html              # all services overview
residential-grading.html   # service detail page
brush-cutting.html         # service detail page
retaining-walls.html       # service detail page
contact.html               # lead capture form + contact info
css/style.css              # all styles
js/main.js                 # mobile nav toggle + footer year
img/                       # logo and images
```

## Lead capture form

The form on `contact.html` posts to [Formspree](https://formspree.io), which
works on static hosting with no backend:

1. Create a free Formspree account (50 submissions/month on the free tier).
2. Create a new form pointed at `jsbgrading@gmail.com`.
3. In `contact.html`, replace `YOUR_FORM_ID` in the form's `action` attribute
   with the real form ID.

Until that's done, the form will not deliver submissions — the call/email
links still work regardless.

## Deploying to GitHub Pages

1. Create a new repository on GitHub (e.g. `jsb-grading-website`).
2. Push this folder to it:

   ```sh
   git remote add origin https://github.com/<your-username>/jsb-grading-website.git
   git push -u origin main
   ```

3. On GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to "Deploy from a branch",
   choose the `main` branch and `/ (root)` folder, then save.
5. The site goes live within a minute or two at
   `https://<your-username>.github.io/jsb-grading-website/`.

### Custom domain (jsbgrading.com)

Once the client approves, point their domain at GitHub Pages:

1. In **Settings → Pages → Custom domain**, enter `www.jsbgrading.com`.
2. At their DNS provider, add a `CNAME` record for `www` pointing to
   `<your-username>.github.io`, and `A` records for the apex domain pointing to
   GitHub Pages' IPs (185.199.108.153, .109.153, .110.153, .111.153).
3. Enable **Enforce HTTPS** after the certificate provisions.

## Notes

- Business details (phone, email, hours, services, testimonials) were sourced
  from the existing site at jsbgrading.com.
