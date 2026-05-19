# Body ReWork — Legal & Support Site

The official static site for **Body ReWork**, containing:

- `index.html` — landing page (links to all legal pages)
- `privacy.html` — Privacy Policy (GDPR + CCPA + KVKK)
- `terms.html` — Terms of Service / EULA (medical disclaimer + Apple subscription rules)
- `support.html` — Support page (FAQs + contact)
- `delete-account.html` — Account deletion guide (Apple 5.1.1(v) compliance)
- `style.css` — shared brand styles

All pages are bilingual (English + Turkish) with a runtime language toggle.

---

## Deploy to Vercel via GitHub

### 1. Create a GitHub repo

```bash
cd body_rework_legal
git init
git add .
git commit -m "Initial commit — Body ReWork legal site"

# Create new repo on github.com (e.g., burakerol/body-rework-legal)
git remote add origin https://github.com/<your-username>/body-rework-legal.git
git branch -M main
git push -u origin main
```

### 2. Deploy with Vercel (no config needed)

1. Go to [vercel.com](https://vercel.com) and sign in with GitHub
2. Click **Add New → Project**
3. Import the `body-rework-legal` repo
4. **Framework Preset**: leave as **Other** (Vercel auto-detects static HTML)
5. **Root Directory**: `./` (default)
6. **Build Command**: leave empty
7. **Output Directory**: leave empty
8. Click **Deploy**

Vercel gives you a free URL like `body-rework-legal.vercel.app` in ~30 seconds.

### 3. (Optional) Connect custom domain

If you own `bodyrework.app`:

1. In Vercel project → **Settings → Domains**
2. Add `bodyrework.app` and `www.bodyrework.app`
3. Vercel shows you DNS records to add at your domain registrar
4. Once propagated (5 min – 24 hours), the site is live on your domain

---

## App Store Connect — URLs to provide

When submitting Body ReWork to App Store Connect, fill these fields:

| Field | URL |
|---|---|
| **Privacy Policy URL** | `https://bodyrework.app/privacy.html` |
| **Support URL** | `https://bodyrework.app/support.html` |
| **Marketing URL** *(optional)* | `https://bodyrework.app/` |
| **Terms of Service URL** *(In-App Purchase setup)* | `https://bodyrework.app/terms.html` |
| **Account Deletion** *(in-app + this page)* | `https://bodyrework.app/delete-account.html` |

If using Vercel default domain, replace `bodyrework.app` with `your-project.vercel.app`.

---

## Email setup (recommended)

The site references these email addresses:

- `burakerolonline@gmail.com` — single inbox for all contact (support, privacy, legal, deletion requests, press)

All five contact links on the legal site (support, privacy, legal, delete-account, hello) currently point to the same Gmail address. This is fine for App Store review — Apple only requires that the contact email actually works.

**Optional upgrade later:** If you buy `bodyrework.app` or another custom domain, you can switch to per-role addresses (`support@`, `privacy@`, etc.) using:

1. **Cloudflare Email Routing** *(free)*: routes all `*@yourdomain.com` to one personal inbox
2. **Google Workspace** ($6/month): real mailboxes
3. **Zoho Mail Free** (free for up to 5 users)

---

## Pre-launch checklist

Before submitting Body ReWork to the App Store, verify:

- [ ] Site deployed and accessible from a public URL
- [ ] All 5 pages load without errors
- [ ] Language toggle works (EN ↔ TR)
- [ ] All internal links work (privacy → terms → support → delete-account)
- [ ] Contact email actually receives mail (test by sending yourself one)
- [ ] Privacy policy mentions every third-party SDK in the app (Firebase, Gemini, Google Sign-In, Apple Sign-In)
- [ ] Account deletion option is documented and works in-app

---

## Things to update before going live

Search-and-replace these placeholders if needed:

| Placeholder | Replace with |
|---|---|
| `bodyrework.app` | Your actual domain |
| `burakerolonline@gmail.com` | Your real support email |
| `Istanbul, Türkiye` (governing law) | Your jurisdiction if different |
| `2026-05-19` (effective date) | The actual launch date |
| `$4.99` / `$29.99` | Final IAP prices (must match App Store Connect setup) |

---

## License

Site code: MIT.
Content (legal text): adapted from common templates — **not legal advice**.
Consult a qualified attorney for production use, especially regarding GDPR/CCPA/KVKK specifics for your jurisdiction.

App icon graphics use [Twemoji](https://github.com/twitter/twemoji) by Twitter, licensed under MIT.
