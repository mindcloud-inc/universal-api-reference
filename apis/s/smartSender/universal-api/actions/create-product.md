# Smart Sender: Create Product

Creates a new product in Smart Sender.

```
POST https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "essences[]": [
    {}
  ],
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "essences[]": [{}],
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryId` | string | no | Category identifier for the product. |
| `essences[]` | array<object> | yes | Array of product essence objects without temporary values. |
| `labels[]` | array<string> | no | Array of label identifiers assigned to the product. |
| `name` | string | yes | Product name, unique within the project. |
| `paymentSystems[]` | array<string> | no | Array of payment system identifiers available for the product. |

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

Through the native Smart Sender API, this operation is `POST /v1/products` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

