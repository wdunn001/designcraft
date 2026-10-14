# Cloud pages, as they render

Six offscreen renders of DesignCraft with cloud storage wired, written by the `renders_for_review`
test in `crates/ui-egui/tests/cloud_files.rs`. The service behind them lives inside the test.

| File | What it shows |
|---|---|
| `designcraft-open-page.png` | Open from the Cloud: your own layouts, and what other people shared |
| `designcraft-open-page-overflow.png` | The overflow menu on one document: Open, Share, Work together |
| `designcraft-save-page.png` | Save to the Cloud: This Computer beside the account, then a folder and a name |
| `designcraft-title-bar-presence.png` | The application bar: the account badge, and who else is here |
| `designcraft-share-split-menu.png` | The Share split button with its chevron pressed |
| `designcraft-share-dialog.png` | The share dialog the label half opens |

Regenerate them with:

```
DESIGNCRAFT_CLOUD_RENDERS=/some/dir cargo test -p designcraft-ui-egui --test cloud_files renders_for_review -- --nocapture
```
