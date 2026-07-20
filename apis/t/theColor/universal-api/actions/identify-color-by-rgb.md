# The Color: Identify Color By RGB

Identifies a color in The Color by RGB value.

```
GET https://connect.mindcloud.co/v1/universal/theColor/latest/actions/identify-color-by-rgb
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Color `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theColor/latest/actions/identify-color-by-rgb?connectionId=$CONNECTION_ID&rgb=0%2C71%2C171" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rgb": "0,71,171"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theColor/latest/actions/identify-color-by-rgb?${params}`, {
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
| `rgb` | string | yes | Valid RGB color, such as 0,71,171 or rgb(0,71,171). Default: `0,71,171`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "self": {
          "href": "https://example.com"
        }
      },
      "cmyk": {
        "value": "string"
      },
      "contrast": {
        "value": "string"
      },
      "hex": {
        "clean": "string",
        "value": "string"
      },
      "hsl": {
        "h": 1,
        "l": 1,
        "s": 1,
        "value": "string"
      },
      "hsv": {
        "value": "string"
      },
      "image": {
        "bare": "https://example.com",
        "named": "https://example.com"
      },
      "name": {
        "closest_named_hex": "Ava Chen",
        "distance": 1,
        "exact_match_name": true,
        "value": "Ava Chen"
      },
      "rgb": {
        "b": 1,
        "g": 1,
        "r": 1,
        "value": "string"
      },
      "XYZ": {
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.self.href` | string | Self link for the color result. |
| `cmyk.value` | string | Formatted CMYK value. |
| `contrast.value` | string | Recommended contrasting color. |
| `hex.clean` | string | Hex value without the leading hash. |
| `hex.value` | string | Formatted hex value. |
| `hsl.h` | number | Hue component. |
| `hsl.l` | number | Lightness percentage. |
| `hsl.s` | number | Saturation percentage. |
| `hsl.value` | string | Formatted HSL value. |
| `hsv.value` | string | Formatted HSV value. |
| `image.bare` | string | SVG image URL without the color name. |
| `image.named` | string | SVG image URL with the color name. |
| `name.closest_named_hex` | string | Closest named hex color. |
| `name.distance` | number | Distance from the closest named color. |
| `name.exact_match_name` | boolean | Whether the supplied color exactly matches the returned name. |
| `name.value` | string | Matched color name. |
| `rgb.b` | number | Blue component. |
| `rgb.g` | number | Green component. |
| `rgb.r` | number | Red component. |
| `rgb.value` | string | Formatted RGB value. |
| `XYZ.value` | string | Formatted XYZ value. |

## Native endpoint

Through the native The Color API, this operation is `GET /id` (base URL `https://www.thecolorapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/identify-color-by-rgb.md) for the provider-specific parameters and requirements.

