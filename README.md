[README.md](https://github.com/user-attachments/files/34007868/README.md)
# Neo Nethengwe — Portfolio

A graphic-design portfolio website: a homepage, six project case studies, an about
page, and a contact page.

**Live site:** https://mnmnethengwe.app

## What's inside

| Path | Purpose |
| --- | --- |
| `src/routes/` | One file per page: `index.tsx` (home), `about.tsx`, `contact.tsx`, `work.$slug.tsx` (case studies), `sitemap[.]xml.ts` |
| `src/lib/portfolio.ts` | All project text and image references — edit this to add or change a project |
| `src/components/` | Shared header and footer |
| `public/media/` | Project images, the portrait, and the downloadable portfolio PDF |
| `src/styles.css` | Colours, fonts, and layout rules |

## Running it locally

You need Node.js 20 or newer.

```sh
npm install
npm run dev
```

Open the address it prints (usually http://localhost:8080).

To make a production build: `npm run build`, then `npm run preview`.

`bun install` and `bun run dev` also work — `bun.lock` is included.

## Adding or changing a project

Open `src/lib/portfolio.ts`. Each project is one entry with a title, category, year,
cover image, detail image, brief, process steps, and outcome. Put the new image in
`public/media/` and point the entry at it. The case-study page, the homepage grid, and
the sitemap all pick the entry up automatically.

## Environment

The site runs as-is with no configuration. `.env` is only relevant if you later build
features that use the backend (logins, stored data); copy `.env.example` to `.env` and
fill in the values from your backend settings.

## Deployment

The project server-renders, so choose a host that runs Node or edge functions rather
than a static-only host — Vercel, Netlify, and Cloudflare Pages all work. Build command
`npm run build`, output `.output/`.

## Built with

TanStack Start (React 19), Tailwind CSS v4, and shadcn/ui primitives. The site was
built and is maintained in [Lovable](https://lovable.dev), which keeps this repository
in sync with the editor.
