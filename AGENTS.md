<!-- BEGIN:nextjs-agent-rules -->

## This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` (resolved from this file's directory; in monorepos the `next` package may not be visible from the repo root) before writing any code. Heed deprecation notices.

This block is written and re-added by `next dev` — verify at `node_modules/next/dist/server/lib/generate-agent-files.js`. Removing it from a diff only re-creates the uncommitted change; committing it with your work keeps the tree clean.

<!-- END:nextjs-agent-rules -->

## Project notes

- VU StudyHub: a Next.js 16 (App Router, JavaScript, Tailwind CSS v4) study portal for Virtual University students. See README.md for the feature list and file layout.
- All course and resource data is static in `src/data/coursesData.js`; there is no backend or database.
- Hosted on Netlify. `netlify.toml` runs `npm ci --include=dev && npm run build` (deploys start without `node_modules`) and publishes `.next`; Netlify's Next.js runtime handles SSR and routing automatically, so no adapter config is needed.
- The "Request / Upload file" modal (`src/components/RequestFileModal.jsx`) only shows a success toast. Submissions are not stored yet. If you persist them, use Netlify Forms or Netlify Database.
