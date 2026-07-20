# WEBLUCY: Update Product

Updates an existing product in WEBLUCY.

```
PUT https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The product ID. |
| `variants[]` | array<object> | no | The product variants carrying pricing and inventory details. |

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

Through the native WEBLUCY API, this operation is `PUT /products/{id}` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

