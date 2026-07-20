# Generate Color Scheme By HSL with The Color

Generates a color scheme in The Color from an HSL seed.

## Endpoint

- **Method:** `GET`
- **Path:** `/scheme`
- **Base URL:** `https://www.thecolorapi.com`
- **Official documentation:** [Generate Color Scheme By HSL](https://www.thecolorapi.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hsl` | query | `string` | yes | Valid HSL seed color, such as 215,100%,34% or hsl(215,100%,34%). |
| `mode` | query | `list<string>` | no | Scheme mode to generate from the seed color. Accepted values: `analogic`, `analogic-complement`, `complement`, `monochrome`, `monochrome-dark`, `monochrome-light`, `quad`, `triad`. |
| `count` | query | `number` | no | Number of colors to return. |
