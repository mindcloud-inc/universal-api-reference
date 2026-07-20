# The Color: Generate Color Scheme By Hex

Generates a color scheme in The Color from a hex seed.

```
GET https://connect.mindcloud.co/v1/universal/theColor/latest/actions/generate-color-scheme-by-hex
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Color `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theColor/latest/actions/generate-color-scheme-by-hex?connectionId=$CONNECTION_ID&hex=0047AB" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hex": "0047AB"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theColor/latest/actions/generate-color-scheme-by-hex?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hex` | string | yes | Valid hex seed color code, such as 0047AB. Default: `0047AB`. |
| `mode` | list<string> | no | Scheme mode to generate from the seed color. One of: `analogic`, `analogic-complement`, `complement`, `monochrome`, `monochrome-dark`, `monochrome-light`, `quad`, `triad`. Default: `monochrome`. |
| `count` | number | no | Number of colors to return. Default: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "schemes": {},
        "self": "https://example.com"
      },
      "colors": [
        [
          {}
        ]
      ],
      "count": "string",
      "image": {
        "bare": "https://example.com",
        "named": "https://example.com"
      },
      "mode": "string",
      "seed": {
        "hex": {
          "value": "string"
        },
        "name": {
          "value": "Ava Chen"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.schemes` | object | Links for alternate scheme modes. |
| `_links.self` | string | Self link for this scheme. |
| `colors[]` | array<object> | Generated colors in the scheme. |
| `count` | string | Number of colors returned by the API. |
| `image.bare` | string | SVG scheme image URL without names. |
| `image.named` | string | SVG scheme image URL with names. |
| `mode` | string | Scheme mode used for generation. |
| `seed` | object | Seed color used to generate the scheme. |
| `seed.hex.value` | string | Seed hex value. |
| `seed.name.value` | string | Seed color name. |

## Native endpoint

Through the native The Color API, this operation is `GET /scheme` (base URL `https://www.thecolorapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-color-scheme-by-hex.md) for the provider-specific parameters and requirements.

