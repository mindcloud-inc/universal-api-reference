# Smart Sender: Update Product

Updates an existing product in Smart Sender.

```
PUT https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryId` | string | no | Updated category identifier for the product. |
| `essences[]` | array<object> | no | Updated array of product essence objects without temporary values. |
| `labels[]` | array<string> | no | Updated array of label identifiers assigned to the product. |
| `name` | string | no | Updated product name, unique within the project. |
| `paymentSystems[]` | array<string> | no | Updated array of payment system identifiers available for the product. |
| `productId` | string | yes | The Smart Sender product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "essences": [
        {}
      ],
      "id": 1,
      "labels": [
        {}
      ],
      "name": "Ava Chen",
      "paymentSystems": [
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
| `category` | object |  |
| `createdAt` | date |  |
| `essences` | array<object> |  |
| `id` | number |  |
| `labels` | array<object> |  |
| `name` | string |  |
| `paymentSystems` | array<object> |  |

## Native endpoint

Through the native Smart Sender API, this operation is `PUT /v1/products/:productId` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

