# The Tipsy Trout Taproom

Website for The Tipsy Trout Taproom in Delta, Colorado, with the El Pollo food truck kitchen.

## How it deploys

Every push to `main` deploys the site to Cloudflare automatically via the GitHub Action in `.github/workflows/deploy.yml` (Wrangler, serving static files from `public/`).

Two repository secrets are required (Settings > Secrets and variables > Actions):

- `CLOUDFLARE_API_TOKEN`: an API token scoped to this Cloudflare account with the permission `Account > Workers Scripts > Edit`. Create it at Cloudflare dashboard > My Profile > API Tokens > Create Token > Create Custom Token.
- `CLOUDFLARE_ACCOUNT_ID`: found on the Cloudflare dashboard, Workers & Pages overview page, right sidebar.

Until a custom domain is connected, the site is live at the `trout-website` workers.dev URL shown in Cloudflare under Workers & Pages.

## Editing the site

The whole site is currently one file: `public/index.html`. Edit it, push to `main`, and the change is live in about a minute.
