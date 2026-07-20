# Generate Color Scheme By CMYK with The Color

Generates a color scheme in The Color from a CMYK seed.

## Endpoint

- **Method:** `GET`
- **Path:** `/scheme`
- **Base URL:** `https://www.thecolorapi.com`
- **Official documentation:** [Generate Color Scheme By CMYK](https://www.thecolorapi.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cmyk` | query | `string` | yes | Valid CMYK seed color, such as 100,58,0,33 or cmyk(100,58,0,33). |
| `mode` | query | `list<string>` | no | Scheme mode to generate from the seed color. Accepted values: `analogic`, `analogic-complement`, `complement`, `monochrome`, `monochrome-dark`, `monochrome-light`, `quad`, `triad`. |
| `count` | query | `number` | no | Number of colors to return. |
