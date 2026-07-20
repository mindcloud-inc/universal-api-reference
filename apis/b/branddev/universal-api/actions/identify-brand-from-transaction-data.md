# Brand.dev: Identify Brand from Transaction Data

Identifies a brand from transaction data in Brand.dev.

```
GET https://connect.mindcloud.co/v1/universal/branddev/latest/actions/identify-brand-from-transaction-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brand.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/identify-brand-from-transaction-data?connectionId=$CONNECTION_ID&transactionInfo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionInfo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/identify-brand-from-transaction-data?${params}`, {
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
| `transactionInfo` | string | yes | Transaction data string to identify a brand from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": {
        "address": {
          "city": "string",
          "country": "string"
        },
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
        "description": "string",
        "domain": "string",
        "email": "ava@example.com",
        "industries": {},
        "isNsfw": true,
        "links": {},
        "logos": [
          [
            {}
          ]
        ],
        "phone": "string",
        "slogan": "string",
        "socials": [
          [
            {}
          ]
        ],
        "stock": {},
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
| `brand.address` | object |  |
| `brand.address.city` | string |  |
| `brand.address.country` | string |  |
| `brand.backdrops[]` | array<object> |  |
| `brand.colors[]` | array<object> |  |
| `brand.colors[].hex` | string |  |
| `brand.colors[].name` | string |  |
| `brand.description` | string |  |
| `brand.domain` | string |  |
| `brand.email` | string |  |
| `brand.industries` | object |  |
| `brand.isNsfw` | boolean |  |
| `brand.links` | object |  |
| `brand.logos[]` | array<object> |  |
| `brand.logos[].mode` | string |  |
| `brand.logos[].url` | string |  |
| `brand.phone` | string |  |
| `brand.slogan` | string |  |
| `brand.socials[]` | array<object> |  |
| `brand.stock` | object |  |
| `brand.title` | string |  |
| `code` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Brand.dev API, this operation is `GET /brand/transaction_identifier` (base URL `https://api.brand.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/identify-brand-from-transaction-data.md) for the provider-specific parameters and requirements.

