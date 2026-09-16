# pigwars-legal

Public legal pages for **PigWars**, served by GitHub Pages so Google Play has a
stable URL to link to.

- Privacy Policy — <https://cfournel.github.io/pigwars-legal/privacy/>

This repository is public on purpose: Google Play requires the privacy policy to
be reachable without signing in, and keeping it in its own repository means the
game repository can stay private.

## Editing

Plain HTML, no build step. Edit and push; Pages redeploys in about a minute.

When the policy changes in substance, update the "Last updated" date in
`privacy/index.html`. Previous wording stays in this repository's git history,
which is what the policy's own "Changes" section points readers at.

## Keeping it truthful

The policy describes what the game actually does today. Two claims in it are the
ones most likely to go stale, and both are load-bearing for the Play Data safety
form:

- **No advertising.** `client/Assets/Scripts/Core/Ads/` in the game repo is an
  integration seam with no SDK behind it. The moment a mediation SDK is wired
  in, this policy and the Data safety entry both have to change *before* that
  build ships.
- **No analytics.** Analytics are disabled in `UnityConnectSettings.asset`.
  Enabling them is likewise a policy change.
