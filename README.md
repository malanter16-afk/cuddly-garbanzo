# Nurture International School: Awards & Accolades 2026 flex banner kit

## What's inside

| Folder / file | What it is |
|---|---|
| `print/Nurture_Awards_Banner_8x4ft.pdf` | **Send this to the flex printer.** 8 ft × 4 ft page, vector text, images embedded. |
| `print/Nurture_Awards_Banner_8x4ft_100dpi.jpg` | Same banner as one big JPG (9600 × 4800 px = 100 DPI at 8×4 ft). Some printers prefer JPG. |
| `print/Nurture_Awards_Banner_preview.jpg` | Small preview for WhatsApp, approvals and sharing. |
| `upscaled/` | Every award photo upscaled 4× with Real-ESRGAN (AI upscaler), plus the extracted school logo. |
| `originals/` | The cropped originals (before upscaling), for comparison. |
| `chatgpt_prompts.md` | Ready-made prompts for ChatGPT image generation: studio "trophy shots", framed-award looks, an enhance-only prompt for people photos, and a logo redraw. |
| `banner/` | Editable source: `banner.html` plus `img/`. Change the text and re-render. |

## Print notes for the flex shop

- **Size:** 8 ft × 4 ft (96 × 48 in) landscape, 100 DPI. That's plenty for flex viewed from 1 m or more.
- **Safe margin:** all text and logos sit at least ~2.5 in from the edge, so eyelets, pipe pockets or stitching won't cut anything.
- **Colour:** the file is RGB. Most flex shops convert it themselves. If they ask for CMYK, they can convert in their RIP.
  The deep navy and gold will print slightly darker on flex than on screen, which is normal.
- **Other sizes:** the layout is 2:1, so it scales straight to **10 × 5 ft** or **6 × 3 ft** with no changes. Just tell the printer the size.

## Please double-check before printing

- **"PATH Movement Award – For Transforming Education":** the trophy shows only the PATH logo, so confirm the exact award name.
- **"Ranked #6 of 6,771 Schools in Bengaluru" (EduConnectIn Ratings):** taken from the old poster. The EduConnectIn awards
  page I checked doesn't show this rank, so confirm it's still current.
- **Best Director / Best Chairman / Gurugauravam / GETI World Summit:** taken from the old poster, with no separate photo provided.
  The Gurugauravam and GETI photos are small thumbnails cut from that poster. They're upscaled, but if you have
  the original photos, send them and they'll look much better.
- **True Gem:** verified on educonnectin.com as "Best School of East Bengaluru, 2026–27, one of 5 winners from 776 schools".

## Editing and re-rendering

Requires Node + Playwright (Chromium).

```bash
cd banner
node render.js preview   # quick look   -> banner_preview.png
node render.js print     # 9600x4800    -> banner_print.png
node render.js pdf       # 8x4 ft PDF   -> banner.pdf
```

To swap a photo (for example, a ChatGPT-improved trophy shot), save it over the file with the same name in `banner/img/` and re-render.
Trophy frames are 4:5 portrait. Any photo works, because it's fitted inside the frame over a blurred copy of itself.
