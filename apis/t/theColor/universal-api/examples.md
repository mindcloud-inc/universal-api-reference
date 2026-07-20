# The Color Universal API Examples

These examples use the MindCloud API key and The Color connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Color Scheme By CMYK

Generates a color scheme in The Color from a CMYK seed.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theColor/latest/actions/generate-color-scheme-by-cmyk?connectionId=$CONNECTION_ID&cmyk=100%2C58%2C0%2C33" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cmyk": "100,58,0,33"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theColor/latest/actions/generate-color-scheme-by-cmyk?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Generate Color Scheme By CMYK action reference](actions/generate-color-scheme-by-cmyk.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/theColor/latest/actions/generate-color-scheme-by-cmyk).
