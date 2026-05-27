# Subtex StatusPage Customization

Drop-in brand styling for **https://subtex.statuspage.io/** that matches getsubtex.com.

## Preview locally

Open `preview.html` in a browser. It mocks Statuspage's markup so you can see
the result before pasting anything into the admin.

## Install on Statuspage

Statuspage exposes three customization slots. Paste each file into its match:

| File | Statuspage slot |
|---|---|
| `page-header.html` | Customization → **Page Header HTML** |
| `custom.css`       | Customization → **CSS** |
| `page-footer.html` | Customization → **Page Footer HTML** |

There is no separate "Head Code" slot — the `<link>` / `<meta>` tags for the
font and favicon live at the top of `page-header.html` and work fine from
there.

Save and reload the public status page.

## Notes

- Uses the same Montserrat font and brand variables as the marketing site
  (`--twilight`, `--marigold`, `--lionsmane`, `--celeste`, `--herb`).
- `.page-status` is restyled into the twilight-blue hero with a left accent
  stripe whose color reflects the current status (green/yellow/orange/red/blue).
- Component status chips reuse the brand palette (herb = operational,
  marigold = degraded, red = major outage, twilight = maintenance).
- The 90-day per-component uptime meters and overall uptime summary are
  preserved and restyled — never hidden. Bar colors map to the same
  palette as the status chips.
- Statuspage's default "Powered by" footer is kept but muted, since the
  brand footer is rendered above it via the Page Footer slot.
- If Statuspage changes its DOM, only `custom.css` needs adjusting — the
  header/footer slots are self-contained and use `sx-` prefixed classes.
