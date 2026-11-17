# Kahvila Kiikku website

Next.js + CSS project for Kahvila Kiikku and Hupikioski.

## Local development

```bash
npm install
npm run dev
```

Open http://localhost:3000

## Production build

```bash
npm run build
npm start
```

## Deploy to Vercel

1. Push this folder to GitHub.
2. In Vercel, choose Add New Project.
3. Import the GitHub repository.
4. Framework preset: Next.js.
5. Deploy.

## Content notes

- Opening hours are currently placeholder text in the top bar and Location section.
- Oiva report link is currently a placeholder in the footer. Replace `href="#"` with the actual Oiva URL or PDF path.
- Hupikioski links to `https://teatteri.kiikku.fi`.
- Private event inquiries use `mailto:kahvilakiikku@gmail.com`.
- Catering is a separate QuickBar shop. It appears in the nav and as a
  **Tilaa catering** section only when `NEXT_PUBLIC_CATERING_SHOP_URL` is set
  at build time. Production kiikku.fi stays unchanged until that env is set.

  Staging shop (current demo):

  `NEXT_PUBLIC_CATERING_SHOP_URL=https://staging.quickbar.fi/shop/kiikun-catering-test`

  Set it first on a Kiikku Preview/test deployment. Do not iframe the shop,
  and do not point it at teatteri.kiikku.fi. A later `catering.kiikku.fi`
  hostname needs a separate DNS decision.
