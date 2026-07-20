# WEBLUCY: Create Product

Creates a new product in WEBLUCY.

```
POST https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "type": "string",
  "variants[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "type": "string",
    "variants[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The product title. |
| `type` | string | yes | The product type: physical, digital, service, or membership. |
| `variants[]` | array<object> | yes | The product variants carrying pricing and inventory details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {}
      ],
      "description": "string",
      "hidden": true,
      "id": 1,
      "images": [
        {}
      ],
      "options": [
        {}
      ],
      "seoDescription": "string",
      "subscription": {},
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "variants": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> |  |
| `description` | string |  |
| `hidden` | boolean |  |
| `id` | number |  |
| `images` | array<object> |  |
| `options` | array<object> |  |
| `seoDescription` | string |  |
| `subscription` | object |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `variants` | array<object> |  |

## Native endpoint

Through the native WEBLUCY API, this operation is `POST /products` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

