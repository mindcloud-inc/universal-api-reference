# Copperx: Activate Product

Activates an existing product in Copperx.

```
PUT https://connect.mindcloud.co/v1/universal/copperx/latest/actions/activate-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/activate-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/copperx/latest/actions/activate-product', {
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
| `id` | string | yes | Product ID path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "defaultPrice": {},
      "defaultPriceId": "string",
      "description": "string",
      "id": "string",
      "images": [
        {}
      ],
      "isActive": true,
      "metadata": {},
      "name": "Ava Chen",
      "unitLabel": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "visibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `defaultPrice` | object |  |
| `defaultPriceId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `images` | array<object> |  |
| `isActive` | boolean |  |
| `metadata` | object |  |
| `name` | string |  |
| `unitLabel` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `visibility` | number |  |

## Native endpoint

Through the native Copperx API, this operation is `POST /products/{id}/activate` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/activate-product.md) for the provider-specific parameters and requirements.

