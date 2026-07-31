# Generate Avatar Image with DiceBear

## Endpoint

- **Method:** `GET`
- **Path:** `/:styleName/:format`
- **Base URL:** `https://api.dicebear.com/10.x`
- **Official documentation:** [Generate Avatar Image](https://www.dicebear.com/how-to-use/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleName` | path | `string` | yes | A current DiceBear 10.x style name in lowercase, using hyphens for multiple words (for example, adventurer-neutral). |
| `format` | path | `list` | yes | Output format. JSON metadata is provided by Get Avatar Metadata. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `seed` | query | `string` | no | Seed value used to generate a deterministic avatar. |
| `flip` | query | `list` | no | Optional flip: none, horizontal, vertical, or both. Accepted values: `0`, `1`, `2`, `3`. |
| `rotate` | query | `number` | no | Optional rotation in degrees from -360 to 360. |
| `scale` | query | `number` | no | Optional scale from 0 to 10. |
| `borderRadius` | query | `number` | no | Optional border radius from 0 to 50. |
| `backgroundColor` | query | `string` | no | Optional hexadecimal background color (for example, b6e3f4). |
