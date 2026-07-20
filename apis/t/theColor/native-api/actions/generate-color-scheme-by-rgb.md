# Generate Color Scheme By RGB with The Color

Generates a color scheme in The Color from an RGB seed.

## Endpoint

- **Method:** `GET`
- **Path:** `/scheme`
- **Base URL:** `https://www.thecolorapi.com`
- **Official documentation:** [Generate Color Scheme By RGB](https://www.thecolorapi.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rgb` | query | `string` | yes | Valid RGB seed color, such as 0,71,171 or rgb(0,71,171). |
| `mode` | query | `list<string>` | no | Scheme mode to generate from the seed color. Accepted values: `analogic`, `analogic-complement`, `complement`, `monochrome`, `monochrome-dark`, `monochrome-light`, `quad`, `triad`. |
| `count` | query | `number` | no | Number of colors to return. |
