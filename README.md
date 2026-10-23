# avinashsaraswat.github.io

The personal site of Avi Saraswat. An index of public work, writing and code.

Plain HTML and CSS. No framework, no build step, no analytics, no tracking. Light and dark follow the system setting.

## Files

- `index.html`, the home page with four featured items
- `work.html`, the index of public work
- `writing.html`, the series schedule and the takes list
- `about.html`, the About text and the disclosure line
- `style.css`, the one stylesheet
- `404.html`, the not-found page
- `.nojekyll`, tells GitHub Pages to serve the files as they are

## Preview locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000 in a browser.

## Custom domain, for later

Once a domain is bought:

1. Verify the domain for the account first, before any DNS record points at GitHub. In the account settings, open Pages, click "Add a domain" and enter the domain. Add the TXT record GitHub shows at the DNS provider, then click Verify. Then no other GitHub account can take it over if it is ever unlinked from this repository. That can happen when the repository is renamed or deleted, or Pages is turned off.
2. Add a file named `CNAME` at the repository root containing only the domain, for example `example.com`. Commit and push it.
3. At the DNS provider, add four A records for the apex domain, pointing at the GitHub Pages addresses `185.199.108.153`, `185.199.109.153`, `185.199.110.153` and `185.199.111.153`. Add a CNAME record for `www` pointing at `avinashsaraswat.github.io`. Do not add a wildcard record such as `*.example.com`, because verification does not protect against it.
4. In the repository's Pages settings, enter the domain under Custom domain, wait for the DNS check to pass, then tick "Enforce HTTPS".

The 404 page uses absolute paths from the site root, so it works at both addresses.

## Updating

Edit the HTML, commit and push. GitHub Pages serves `main` from the root at https://avinashsaraswat.github.io and redeploys on each push.

- When a series piece or a take is live, mark it published on `writing.html`, and on `index.html` for a featured piece, with its link.
- When a new fsi-eval-harness version ships, update the release link and the version DOI on `work.html` and `index.html`. The concept DOI stays.
- A role or a credit appears here only where a public page shows it, with that page's link.
