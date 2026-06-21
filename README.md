# DHEVYL GROUP - Luxury Services Website

![React](https://img.shields.io/badge/React-18.2-61DAFB?style=for-the-badge&logo=react&logoColor=061B22)
![TypeScript](https://img.shields.io/badge/TypeScript-5.5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-5.4-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.4-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-Lead_CRM-3FCF8E?style=for-the-badge&logo=supabase&logoColor=053B2B)
![Vercel](https://img.shields.io/badge/Vercel-Deployment-000000?style=for-the-badge&logo=vercel&logoColor=white)

A production website for DHEVYL GROUP SRL, a luxury business services company operating across property management, design, e-commerce, video production, yacht concierge, and premium laundry services.
The project replaced a fragmented brand presence with a fast, SEO-oriented React application that presents every division, captures qualified enquiries, and gives the team an authenticated lead-management dashboard.

## Project Preview

![DHEVYL GROUP project preview](public/image/foto-e.jpg)

The PWA manifest is already configured for desktop, tablet, and mobile screenshots at `public/image/screenshot-desktop.png`, `public/image/screenshot-tablet.png`, and `public/image/screenshot-mobile.png`. Those capture files are not currently committed, so this README uses a real visual asset shipped with the live site.

## Tech Stack

![React](https://img.shields.io/badge/Frontend-React-61DAFB?style=flat-square&logo=react&logoColor=061B22)
![TypeScript](https://img.shields.io/badge/Language-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Build-Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/UI-TailwindCSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Supabase](https://img.shields.io/badge/Data-Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=053B2B)
![Prisma](https://img.shields.io/badge/Schema-Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![React Router](https://img.shields.io/badge/Routing-React_Router-CA4245?style=flat-square&logo=reactrouter&logoColor=white)
![Vercel](https://img.shields.io/badge/Hosting-Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

## Core Features

- Interactive luxury-services homepage with carousel navigation across the D, H, E, V, Y, and L divisions.
- Division detail experience with anchor navigation, branded logos, sector-specific imagery, and external portals for each business unit.
- Italian and English copy managed through a lightweight `LanguageContext`, keeping the public pages bilingual without adding CMS overhead.
- Supabase-backed contact form with a `mailto:` fallback, so lead capture still works when the database request fails.
- Authenticated admin dashboard for reviewing leads, filtering contacts, and moving enquiries through `new`, `in-progress`, `completed`, and `cancelled` states.

## Architecture

The application is a client-rendered Vite SPA deployed behind a Vercel rewrite that routes all non-asset requests back to `index.html`.

- `src/pages` contains route-level screens: home, divisions, contact, legal pages, admin login, and admin dashboard.
- `src/components/sections` holds the marketing sections used by the homepage, including hero, partners, metrics, and CTA blocks.
- `src/context/LanguageContext.tsx` provides the active `IT` or `EN` locale and resolves nested translation keys from `src/translations`.
- `src/lib/supabase.ts` centralizes browser-side Supabase access and supports both `VITE_` and `NEXT_PUBLIC_` environment naming.
- `supabase/migrations` and `prisma/schema.prisma` document the `contacts` data model used by the form and admin workflow.
- `public` contains deployment assets, SEO files, the web manifest, service worker, partner logos, and brand imagery.

## Results And Impact

- Live project: [dhevylgroup.com](https://dhevylgroup.com)
- Consolidated six luxury-service divisions into one navigable brand platform instead of separate disconnected entry points.
- Turned the contact page into an operational lead pipeline with persistent storage, authenticated review, search, filtering, and status updates.
- Added production SEO foundations: structured data, canonical metadata, sitemap, robots file, PWA manifest, and social preview configuration.
- Prepared the app for Vercel deployment with SPA fallback routing and build commands based on TypeScript plus Vite.

## Development

```bash
npm install
npm run dev
npm run build
npm run lint
```

Required environment variables:

```bash
VITE_SUPABASE_URL=
VITE_SUPABASE_ANON_KEY=
DATABASE_URL=
DIRECT_URL=
```

## Contacts And Portfolio

- Website: [dhevylgroup.com](https://dhevylgroup.com)
- Email: [info@dhevylgroup.com](mailto:info@dhevylgroup.com)
- LinkedIn: [DHEVYL GROUP](https://www.linkedin.com/company/dhevyl-group)
- Instagram: [@d_h_e_v_y_l_](https://www.instagram.com/d_h_e_v_y_l_/)

This repository is structured as a portfolio case study for a real luxury-services web platform: brand presentation, lead capture, admin workflow, SEO, and production deployment in a single codebase.
