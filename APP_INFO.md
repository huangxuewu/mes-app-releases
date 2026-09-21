# Edit app information without an APK release

MES Store 1.2.19 and later read [`app-info.json`](app-info.json) directly from this
public GitHub repository. Edit that file on the **main** branch and commit the change.
Pull down on Featured or Apps in MES Store to see it. Automatic checks also fetch it.
GitHub's raw-content cache can take a few minutes to serve a new commit.

Each object in `apps` belongs to the Android `packageName`, which must stay unchanged.

| Field | Where it appears | Maximum length |
| --- | --- | --- |
| `name` | App name throughout the store | 80 |
| `intro` | App list, search, and app details | 280 |
| `featured.eyebrow` | Small heading on the Featured card | 60 |
| `featured.headline` | Main Featured headline; `\n` adds a line break | 100 |
| `featured.description` | Supporting Featured paragraph | 600 |
| `featured.actionLabel` | Featured card action, which opens app details | 32 |
| `link.label` | External website/help button on app details | 60 |
| `link.url` | HTTPS website or help-page destination | 2048 |

Use `"link": null` or remove `link` to hide the external button. Links must use HTTPS,
without embedded credentials or custom ports. The default destinations are the
editable Markdown pages in [`help/`](help/); replace them with your own website URLs
at any time. Use public information only: this repository and its content are public.

Keep `schemaVersion` at `1`, use valid JSON, and include all four Featured text fields
for each entry. Invalid content is rejected as a whole and the last valid copy is kept.
On first launch without a network, the app uses its bundled copy. An app missing from
this file uses its catalog name and description with a generic Featured heading.

This file cannot change APK downloads, versions, checksums, or signing certificates.
Those remain in `catalog.json` and the verified release workflow. The app's screenshot
images/captions, icons, card artwork, and layout are still bundled in the APK.
Publishing another APK does not change this editorial file.

Write each app's introduction around a concrete reason to use it. Give Featured its
own headline and paragraph instead of repeating the list introduction. Match the
voice to the work: dispatch planning, a quick conversation, a production shift,
shipment paperwork, or a personal time record.
