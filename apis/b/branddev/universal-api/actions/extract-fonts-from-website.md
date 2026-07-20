# Brand.dev: Extract Fonts from Website

Retrieves website font data from Brand.dev.

```
GET https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-fonts-from-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brand.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-fonts-from-website?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/extract-fonts-from-website?${params}`, {
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
| `domain` | string | yes | Domain name to extract fonts from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "domain": "string",
      "fonts": [
        [
          {}
        ]
      ],
      "status": "string"
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
| `fonts[]` | array<object> |  |
| `fonts[].fallbacks[]` | array<string> |  |
| `fonts[].font` | string |  |
| `fonts[].numElements` | number |  |
| `fonts[].numWords` | number |  |
| `fonts[].percentElements` | number |  |
| `fonts[].percentWords` | number |  |
| `fonts[].uses[]` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Brand.dev API, this operation is `GET /brand/fonts` (base URL `https://api.brand.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-fonts-from-website.md) for the provider-specific parameters and requirements.

