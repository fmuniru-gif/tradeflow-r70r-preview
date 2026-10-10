# ZEZMS isolated preview: r70Q to r70R (test only)

This is an **initial r70Q baseline** for a separate, new GitHub Pages repository named `tradeflow-r70r-preview`. It is **NOT** the r70R release and must NEVER replace the files in the operational `tradeflow-zola` repository.

## Safety
- The preview repository and GitHub Pages site are PUBLIC. Do not upload backups, local storage, access tokens, .env files, passphrases, or real operation archives.
- Use a clean separate browser profile, not the browser profile used for TradeFlow.
- Do NOT sign in, pair devices, enter a Supabase URL or key, import a real business backup, or enter any real transaction.
- Do not use the real CAMON 17P Repaired phone for this test.
- Keep operational `tradeflow-zola` main, Pages settings and the existing three running devices unchanged.

## Test procedure (without touching live site)
1. In GitHub Desktop create a *NEW LOCAL REPOSITORY* called `tradeflow-r70r-preview`. Use your normal local GitHub workspace, not the existing `tradeflow-zola` folder.
2. Open its location in Explorer; extract this starter ZIP and copy its contents (all 71 application files and `.nojekyll`) into the NEW repository root. Commit and publish this new repo as PUBLIC. Never publish backups.
3. On GitHub, in this NEW repo only, go to Settings > Pages > Deploy from branch; choose main / (root), Save. Check the resulting site URL under Settings > Pages. Wait until GitHub reports it published.
4. Open preview URL in a clean separate Chrome/Edge profile; inspect the r70Q shell and service worker; do not connect Cloud or enter business data.
5. In the same NEW preview repo, replace ONLY `index.html`, `sw.js`, `manifest.json` with the already verified three-file **r70R** staging candidate, commit and push. Wait for Pages build, refresh the preview profile and check service-worker update, cache version and offline navigation.

## Expected website address (not live until GitHub reports it)
`https://fmuniru-gif.github.io/tradeflow-r70r-preview/`

The real production address stays separate. GitHub Pages does not create a second site for a branch within the same repository.

## Acceptance
- r70Q preview baseline first, then r70R on the SAME preview URL and profile.
- r70R application, manifest and SW show the intended build marker.
- No authenticated Cloud session, business records, queue mutations or external network calls during synthetic testing.
- No new browser console errors from the preservation module.
- Offline shell navigation works after successful new SW install.
- Do NOT merge the staging branch into live `main` yet.

This starter pack has no production secrets in `js/config.js` (Supabase URL and key are blank), but it is still full app source and must be handled like a public source-code deployment.
