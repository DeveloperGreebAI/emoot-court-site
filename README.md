# E-Moot Court: Google Workspace Marketplace pages

Public pages the Marketplace SDK asks for (Store Listing "Support links" and App Configuration
"Developer website URL"). Plain HTML and one CSS file; no build step.

| File | Use in Google Cloud |
|---|---|
| `index.html` | Developer website URL / Application website URL |
| `support.html` | Store Listing -> Support URL |
| `privacy.html` | Store Listing -> Privacy policy URL |
| `terms.html` | Store Listing -> Terms of service URL |

Images for the Store Listing are in `../assets/marketplace/` (this folder keeps copies of the
icons and screenshot only for the pages themselves):

| Store Listing field | File | Size |
|---|---|---|
| Application icon (small) | `emoot-icon-32.png` | 32x32 |
| Application icon (large) | `emoot-icon-128.png` | 128x128 |
| Web app icons (if asked) | `emoot-icon-48.png`, `emoot-icon-96.png` | 48x48, 96x96 |
| Application card banner | `emoot-banner-220x140.png` | 220x140 |
| Screenshot (required, shows the Meet integration) | `emoot-meet-screenshot-1280x800.png` | 1280x800 |

## Publish on GitHub Pages
1. Create a new **public** GitHub repository, for example `emoot-court-site`.
2. Copy **everything in this folder** (including the hidden `.github` folder and `.nojekyll`) to the
   root of that repository and push to `main`.
3. In the repository: **Settings -> Pages -> Build and deployment -> Source: GitHub Actions**.
4. The workflow `.github/workflows/static.yml` deploys on every push. After about a minute the
   site is at `https://<github-user>.github.io/<repository>/`.
5. Open the four pages in a private window to check they load, then paste the URLs into the
   Marketplace SDK.

Any static host works the same way (Cloudflare Pages, Netlify, or a page on greenai.services).

## Before publishing
- Contact address is `developer@greenai.services` on every page; change it if support mail
  should go elsewhere.
- Company name is written as "GreenAI"; use the registered company name if it differs.
- Privacy and terms describe how E-Moot Court works today (Nexus sign-in, transcripts,
  team chat, notes, Meet room creation). Have them checked before the public release, and update
  "Last updated" when anything changes.
