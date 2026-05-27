# Subtex StatusPage Customization

Drop-in brand styling for **https://subtex.statuspage.io/** that matches getsubtex.com.

## Preview locally

Open `preview.html` in a browser. It mocks Statuspage's markup so you can see
the result before pasting anything into the admin.

## Install on Statuspage

In the Statuspage admin, go to **Your page → Customization** and paste each
file into its matching slot:

| File | Statuspage slot |
|---|---|
| `head-code.html`   | Customization → **Head Code** |
| `page-header.html` | Customization → **Page Header** |
| `custom.css`       | Customization → **CSS** |
| `page-footer.html` | Customization → **Page Footer** |

Save and reload the public status page.

## Notes

- Uses the same Montserrat font and brand variables as the marketing site
  (`--twilight`, `--marigold`, `--lionsmane`, `--celeste`, `--herb`).
- `.page-status` is restyled into the twilight-blue hero with a left accent
  stripe whose color reflects the current status (green/yellow/orange/red/blue).
- Component status chips reuse the brand palette (herb = operational,
  marigold = degraded, red = major outage, twilight = maintenance).
- Statuspage's default "Powered by" footer is kept but muted, since the
  brand footer is rendered above it via the Page Footer slot.
- If Statuspage changes its DOM, only `custom.css` needs adjusting — the
  header/footer slots are self-contained and use `sx-` prefixed classes.
