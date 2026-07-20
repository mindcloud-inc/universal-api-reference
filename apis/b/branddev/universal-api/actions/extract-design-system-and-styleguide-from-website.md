# Brand.dev: Extract Design System and Styleguide from Website

Retrieves website styleguide data from Brand.dev.

```
GET https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-design-system-and-styleguide-from-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brand.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-design-system-and-styleguide-from-website?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-design-system-and-styleguide-from-website?${params}`, {
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
| `directUrl` | string | no | Specific URL to fetch the styleguide from directly. |
| `domain` | string | no | Domain name to extract a styleguide from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "domain": "string",
      "status": "string",
      "styleguide": {
        "colors": {
          "accent": "string",
          "background": "string",
          "text": "string"
        },
        "components": {
          "button": {
            "primary": {
              "backgroundColor": "string"
            }
          },
          "card": {
            "backgroundColor": "string"
          }
        },
        "elementSpacing": {},
        "mode": "string",
        "shadows": {},
        "typography": {
          "headings": {
            "h1": {
              "fontFamily": "string"
            }
          },
          "p": {
            "fontFamily": "string"
          }
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
| `code` | number |  |
| `domain` | string |  |
| `status` | string |  |
| `styleguide` | object |  |
| `styleguide.colors` | object |  |
| `styleguide.colors.accent` | string |  |
| `styleguide.colors.background` | string |  |
| `styleguide.colors.text` | string |  |
| `styleguide.components` | object |  |
| `styleguide.components.button` | object |  |
| `styleguide.components.button.primary` | object |  |
| `styleguide.components.button.primary.backgroundColor` | string |  |
| `styleguide.components.card` | object |  |
| `styleguide.components.card.backgroundColor` | string |  |
| `styleguide.elementSpacing` | object |  |
| `styleguide.mode` | string |  |
| `styleguide.shadows` | object |  |
| `styleguide.typography` | object |  |
| `styleguide.typography.headings` | object |  |
| `styleguide.typography.headings.h1` | object |  |
| `styleguide.typography.headings.h1.fontFamily` | string |  |
| `styleguide.typography.p` | object |  |
| `styleguide.typography.p.fontFamily` | string |  |

## Native endpoint

Through the native Brand.dev API, this operation is `GET /brand/styleguide` (base URL `https://api.brand.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-design-system-and-styleguide-from-website.md) for the provider-specific parameters and requirements.

