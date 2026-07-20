# Brand.dev: Retrieve Simplified Brand Data by Domain

Retrieves simplified brand data from Brand.dev by domain.

```
GET https://connect.mindcloud.co/v1/universal/branddev/latest/actions/retrieve-simplified-brand-data-by-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brand.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/retrieve-simplified-brand-data-by-domain?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/retrieve-simplified-brand-data-by-domain?${params}`, {
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
| `domain` | string | yes | Domain name to retrieve simplified brand data for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": {
        "backdrops": [
          [
            {}
          ]
        ],
        "colors": [
          [
            {}
          ]
        ],
        "domain": "string",
        "logos": [
          [
            {}
          ]
        ],
        "title": "string"
      },
      "code": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | object |  |
| `brand.backdrops[]` | array<object> |  |
| `brand.colors[]` | array<object> |  |
| `brand.colors[].hex` | string |  |
| `brand.colors[].name` | string |  |
| `brand.domain` | string |  |
| `brand.logos[]` | array<object> |  |
| `brand.logos[].mode` | string |  |
| `brand.logos[].url` | string |  |
| `brand.title` | string |  |
| `code` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Brand.dev API, this operation is `GET /brand/retrieve-simplified` (base URL `https://api.brand.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-simplified-brand-data-by-domain.md) for the provider-specific parameters and requirements.

