# Calendar App

A modern, interactive calendar application built with Next.js — browse events in a clean weekly view, search your schedule, and inspect event details (time, location, attendees, organizer) in a polished dark-mode-ready UI.

> Originally generated with [v0.app](https://v0.app), then refined and documented.

## Features

- 📅 **Weekly calendar view** with prev/next navigation
- 🔍 **Event search** across titles and descriptions
- ➕ **Add-event UI** flow (dialog with title, time, location, attendees)
- 🗂️ **Event detail panel** — description, location, attendees, organizer
- 🎨 Color-coded events per category
- 🌙 **Dark / light mode** toggle (next-themes)
- 📱 Responsive layout with collapsible sidebar
- ✨ Smooth animations and Lucide iconography

## Tech Stack

- [Next.js](https://nextjs.org/) 15 (App Router, static export)
- [React](https://react.dev/) 19
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/) 3 + `tailwindcss-animate`
- [shadcn/ui](https://ui.shadcn.com/) + [Radix UI](https://www.radix-ui.com/) primitives
- [Lucide React](https://lucide.dev/) icons
- [date-fns](https://date-fns.org/) for date handling

## Quick Start

### Prerequisites

- Node.js 18+ and npm

### Install & run

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Build (static export)

```bash
npm run build
```

The fully static site is emitted to `out/` and can be hosted on any static host (Cloudflare Pages, GitHub Pages, Netlify, Vercel).

## Project Structure

```
calendar-app-wt/
├── app/
│   ├── page.tsx        # Main calendar UI (client component)
│   ├── layout.tsx      # Root layout + theme provider
│   ├── loading.tsx     # Loading state
│   └── globals.css     # Tailwind + global styles
├── components/
│   └── theme-provider.tsx
├── lib/
│   └── utils.ts        # cn() class-name helper
├── public/             # Static assets
├── styles/             # Extra style files
├── next.config.mjs     # output: 'export', unoptimized images
└── tailwind.config.js
```

## Environment Variables

None required — the app is fully client-side with sample event data.

## Deployment

The app is a **static export** (`output: 'export'`), so it deploys to any static host:

- **Cloudflare Pages** — point the build output at `out/`
- **GitHub Pages / Netlify / Vercel** — same, serve the `out/` directory

No server, no API routes, no secrets needed.

## Notes

- Events are sample/demo data stored in component state (`app/page.tsx`). Persisting to localStorage or a backend is a natural next step.
- Lint and TypeScript errors are ignored during builds (v0 default); tighten these before production use if desired.

---

Built by Girish Lade · [ladestack.in](https://ladestack.in)
