# <img src="https://images.mindcloud.co/apps/icons/the-color_1778005492640.png" alt="The Color logo" width="28" height="28"> The Color: Universal API

Identify colors, convert color formats, and generate color schemes using The Color API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/theColor/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.thecolorapi.com/
- **Vendor API docs:** https://www.thecolorapi.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Color Scheme By CMYK](actions/generate-color-scheme-by-cmyk.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theColor/latest/actions/generate-color-scheme-by-cmyk?connectionId=$CONNECTION_ID&cmyk=100%2C58%2C0%2C33" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Color

| Action | Method | Description |
| --- | --- | --- |
| [Identify Color By CMYK](actions/identify-color-by-cmyk.md) | GET | Identifies a color in The Color by CMYK value. |
| [Identify Color By Hex](actions/identify-color-by-hex.md) | GET | Identifies a color in The Color by hex code. |
| [Identify Color By HSL](actions/identify-color-by-hsl.md) | GET | Identifies a color in The Color by HSL value. |
| [Identify Color By RGB](actions/identify-color-by-rgb.md) | GET | Identifies a color in The Color by RGB value. |

### Color Scheme

| Action | Method | Description |
| --- | --- | --- |
| [Generate Color Scheme By CMYK](actions/generate-color-scheme-by-cmyk.md) | GET | Generates a color scheme in The Color from a CMYK seed. |
| [Generate Color Scheme By Hex](actions/generate-color-scheme-by-hex.md) | GET | Generates a color scheme in The Color from a hex seed. |
| [Generate Color Scheme By HSL](actions/generate-color-scheme-by-hsl.md) | GET | Generates a color scheme in The Color from an HSL seed. |
| [Generate Color Scheme By RGB](actions/generate-color-scheme-by-rgb.md) | GET | Generates a color scheme in The Color from an RGB seed. |

