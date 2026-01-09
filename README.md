# Evvl Marketing Site

Marketing site for [Evvl](https://evvl.com) - Compare AI models side by side.

Built with [Astro](https://astro.build) + [Tailwind CSS](https://tailwindcss.com).

## Development

```bash
npm install
npm run dev     # Start dev server at localhost:4321
npm run build   # Build to ./dist/
npm run preview # Preview production build
```

## Deployment

### Vercel Setup

1. Connect this repo to a new Vercel project
2. Framework preset: Astro
3. No environment variables needed
4. Deploy

### Domain Configuration

**DNS Records** (at your domain registrar):

```
# Marketing site (apex domain) - evvl.com
A     @       76.76.21.21

# www redirect
CNAME www     cname.vercel-dns.com.

# App subdomain - app.evvl.com (separate Vercel project)
CNAME app     cname.vercel-dns.com.
```

**Vercel Domain Settings**:

1. Marketing site project: Add `evvl.com` as primary domain
2. App project: Add `app.evvl.com` as domain
3. Vercel handles SSL automatically

## Architecture

```
evvl.com           → This marketing site (Astro)
app.evvl.com       → Evaluation app (Next.js, separate repo)
```

## Pages

- `/` - Landing page with features, how-it-works, privacy
- `/download` - Desktop app download page (links to GitHub releases)
