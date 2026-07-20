# Generate Color Scheme By Hex with The Color

Generates a color scheme in The Color from a hex seed.

## Endpoint

- **Method:** `GET`
- **Path:** `/scheme`
- **Base URL:** `https://www.thecolorapi.com`
- **Official documentation:** [Generate Color Scheme By Hex](https://www.thecolorapi.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hex` | query | `string` | yes | Valid hex seed color code, such as 0047AB. |
| `mode` | query | `list<string>` | no | Scheme mode to generate from the seed color. Accepted values: `analogic`, `analogic-complement`, `complement`, `monochrome`, `monochrome-dark`, `monochrome-light`, `quad`, `triad`. |
| `count` | query | `number` | no | Number of colors to return. |
