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

## Apps

| App | Slug | Privacy | Terms |
| --- | --- | --- | --- |
| Any Video Converter | `videoconverter` | ✅ | ✅ |
| Audio Converter | `audioconverter` | ✅ | ✅ |
| Authik | `authik` | ✅ | ✅ |
| Cleaner11 | `cleaner11` | ✅ | ✅ |
| Duplicate Cleaner | `duplicatecleaner` | ✅ | ✅ |
| MonitorSync | `monitorsync` | ✅ | ✅ |
| PDF Toys | `pdftoys` | ✅ | ✅ |
| Scann | `scann` | ✅ | ✅ |
| Snipik | `snipik` | ✅ | ✅ |
| Volmix | `volmix` | ✅ | ✅ |
| Zipik | `zipik` | ✅ | ✅ |

## Adding a new app

1. Copy the `_template` folder and rename it to your app's slug, e.g.:

   ```
   legal/_template/  ->  legal/mynewapp/
   ```

2. In both `privacy/index.html` and `terms/index.html`, replace the
   placeholders:
   - `[App Name]` — the app's display name
   - `[Month DD, YYYY]` — the "Last updated" date
   - `[one-line description ...]` — what the app does (intro of both pages)
   - `[... list the stores it ships on]` — platforms / stores (Privacy intro)
   - Edit the bracketed `[...]` notes to match what the app actually does
     (what stays on-device, permissions, which SDKs — Firebase / AdMob /
     none — purchases, ads, etc.). The Privacy template assumes the Gemiry
     default of "we collect nothing ourselves"; if an app ever does collect
     data directly, rewrite sections 1, 5 and 7 honestly. Fill in
     the app-specific Terms section (section 3) with the one thing the user
     must take responsibility for, remove any sections that don't apply,
     and renumber the headings.
   - Governing law is already written as worldwide / country of
     establishment with consumer-law carve-out — leave it as is.

3. Add the app to the **Apps** table above.

4. Commit and push. The page is live at the URL pattern above.

> Keep the `_template` folder as-is so it stays available for the next app.
