# VMP-001 · Honda Tester Beta

Static GitHub Pages beta for **Vehicle Maintenance Pro (VMP-001)** focused on Honda vehicles sold in the United States from model years 2015–2026.

## What is in this build

- 77 Honda family/year rows marked `PUBLISHED` in the current research workbook.
- 12 Honda families currently available to public testers.
- 31 public mechanical profiles.
- 9 public maintenance rule sets.
- 120 included Honda source records (119 directly referenced by published rows + the general Honda Maintenance Minder overview).
- Manual year/model/profile selection.
- Optional local-only VIN and odometer.
- Honda Maintenance Minder code decoder based on the selected rule set.
- Official Honda source links for the selected model-year.
- Light/dark mode.
- Mobile layout.
- Local feedback form with Copy and Download JSON buttons.

## Data safety rule

Only annual rows whose status is `PUBLISHED` are exposed to testers. `PARTIAL`, `VERIFIED_PROFILE_PENDING_ANNUAL`, `BLOCKED_SOURCE`, and `NOT_SOLD_US` entries are not selectable.

Normal service timing is **not converted into invented fixed mileage intervals** when the Honda source uses Maintenance Minder. Mileage/month fields are shown only for an official severe-use exception or maximum-time rule captured in the dataset.

## Privacy

No personal VIN or personal odometer is hard-coded in this repository. Optional tester VIN/odometer values are stored in browser `localStorage`; this static beta has no server.

## Files

- `index.html` — tester interface
- `style.css` — responsive light/dark UI
- `vehicles.js` — published Honda annual coverage + mechanical profiles
- `maintenance.js` — normalized maintenance rules + official Honda sources
- `script.js` — selection, Maintenance Minder decoder, local state, source filtering and feedback
- `.nojekyll` — keeps GitHub Pages deployment simple

## Publish as a new GitHub Pages repository

Recommended repository name:

`vmp-honda-beta`

1. In GitHub, create a new **Public** repository named `vmp-honda-beta`.
2. Do not add starter files if you plan to upload this package directly.
3. Upload all files from this folder to the **root** of the repository.
4. Commit to the `main` branch.
5. Open **Settings → Pages**.
6. Under **Build and deployment**, choose **Deploy from a branch**.
7. Select branch `main` and folder `/ (root)`, then Save.
8. For the GitHub account used for VMP, the expected Pages address is:

`https://ezequielmendivil16-alt.github.io/vmp-honda-beta/`

## Tester flow

1. Open the site on phone or desktop.
2. Choose **Find My Honda**.
3. Select model year, Honda family and mechanical profile.
4. Optionally enter odometer/VIN.
5. Open **Maintenance** and enter the code shown by the vehicle (for example `A1` or `B12`).
6. Compare the tasks shown by VMP with the vehicle/owner documentation.
7. Open **Honda Sources** and verify the referenced Honda record.
8. Use **Feedback** to copy or download the report and send it to the VMP project owner.

## Important beta disclaimer

VMP-001 is a maintenance organization and research beta. It does not replace the vehicle's owner manual, Honda Maintenance Minder display, official service information, recall information, diagnosis, inspection, or professional service advice.

## Dataset provenance

Generated from the VMP Honda research workbook `VMP_Honda_2015_2026_revision(3).xlsx`, using only rows marked `PUBLISHED` for the public tester interface.
