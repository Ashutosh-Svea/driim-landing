# Driim Landing Page

A waitlist landing page for Driim — the dream exploration app by Siddha Tantra Arts.

## Quick Deploy to Vercel

### Option 1: Deploy via GitHub (Recommended)

1. **Push this folder to a GitHub repository:**
   ```bash
   cd driim-landing
   git init
   git add .
   git commit -m "Initial landing page"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/driim-landing.git
   git push -u origin main
   ```

2. **Connect to Vercel:**
   - Go to [vercel.com](https://vercel.com) and sign in with GitHub
   - Click "Add New Project"
   - Import your `driim-landing` repository
   - Click "Deploy" (no configuration needed)

3. **Connect your custom domain:**
   - In Vercel dashboard, go to your project → Settings → Domains
   - Add `driim.app` (or your domain)
   - Update your domain's DNS settings as instructed by Vercel

### Option 2: Deploy via Vercel CLI

```bash
npm i -g vercel
cd driim-landing
vercel
```

## Setup Email Collection

The forms currently point to Formspree. To set this up:

1. **Create a Formspree account:** Go to [formspree.io](https://formspree.io)

2. **Create a new form** and copy your form ID (looks like `xyzabcde`)

3. **Replace `YOUR_FORM_ID`** in `index.html` (appears twice):
   ```html
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```
   Change to:
   ```html
   action="https://formspree.io/f/xyzabcde"
   ```

### Alternative: ConvertKit

If you prefer ConvertKit for more advanced email sequences:

1. Create a ConvertKit account
2. Create a Form
3. Get the form action URL from ConvertKit
4. Replace the Formspree URLs with your ConvertKit form URL
5. Update the form field names as needed (ConvertKit uses `email_address`)

## Files

```
driim-landing/
├── index.html      # Main landing page
├── privacy.html    # Privacy policy
├── vercel.json     # Vercel configuration
└── README.md       # This file
```

## Customization

### Add Your Logo/Favicon

1. Create a `favicon.png` (32x32 or 64x64)
2. Create an `og-image.png` for social sharing (1200x630)
3. Place them in this folder

### Analytics

Uncomment and configure the Google Analytics section at the bottom of `index.html`:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
```

### Colors

The color palette is defined in CSS variables at the top of `index.html`:

```css
:root {
    --deep-indigo: #1a1a2e;
    --mystic-purple: #4a3f6b;
    --soft-violet: #7c6a9a;
    --dawn-rose: #d4a5a5;
    --golden-light: #e8c87d;
    --cream: #f5f0e8;
    --soft-white: #fdfcfa;
}
```

## Domain Setup

After deploying to Vercel:

1. Go to your domain registrar (where you bought driim.app)
2. Add the DNS records Vercel provides:
   - Usually an A record pointing to `76.76.21.21`
   - Or a CNAME record pointing to `cname.vercel-dns.com`
3. Wait for DNS propagation (can take up to 48 hours, usually much faster)

## Support

Created by Siddha Tantra Arts, Sweden.
