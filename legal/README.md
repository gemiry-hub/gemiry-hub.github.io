# Legal pages

Per-app **Privacy Policy** and **Terms & Conditions** pages live here. They are
reachable by direct URL but are **not listed anywhere** on the public site, and
they carry a `noindex, nofollow` meta tag (and are disallowed in `robots.txt`)
so app names aren't surfaced by search engines.

## URL pattern

```
https://gemiry.com/legal/<app-slug>/privacy/
https://gemiry.com/legal/<app-slug>/terms/
```

The clean URL comes from the folder + `index.html`. Use these direct links in
each app's store listing and in-app "Privacy" / "Terms" links.

## Adding a new app

1. Copy the `_template` folder and rename it to your app's slug, e.g.:

   ```
   legal/_template/  ->  legal/mynewapp/
   ```

2. In both `privacy/index.html` and `terms/index.html`, replace the
   placeholders:
   - `[App Name]` — the app's display name
   - `[Month DD, YYYY]` — the "Last updated" date
   - `[jurisdiction]` — governing law (Terms only)
   - Edit the bracketed `[...]` notes to match what the app actually does
     (data collected, third-party services, purchases, etc.). Remove any
     sections that don't apply.

3. Commit and push. The page is live at the URL pattern above.

> Keep the `_template` folder as-is so it stays available for the next app.
