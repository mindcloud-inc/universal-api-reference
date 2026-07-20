# Pipedrive: Add Product

Creates a new product in Pipedrive.

```
POST https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productName` | string | yes | Product name. |
| `code` | string | no | Product code. |
| `description` | string | no | Product description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addTime": "string",
      "category": {},
      "code": "string",
      "description": "string",
      "id": 1,
      "isDeleted": true,
      "isLinkable": true,
      "name": "Ava Chen",
      "ownerId": 1,
      "prices": [
        {
          "cost": 1,
          "currency": "string",
          "directCost": 1,
          "notes": "string",
          "price": 1,
          "productId": 1
        }
      ],
      "tax": 1,
      "unit": "string",
      "updateTime": "string",
      "visibleTo": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addTime` | string |  |
| `category` | object |  |
| `code` | string |  |
| `description` | string |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `isLinkable` | boolean |  |
| `name` | string |  |
| `ownerId` | number |  |
| `prices[].cost` | number |  |
| `prices[].currency` | string |  |
| `prices[].directCost` | number |  |
| `prices[].notes` | string |  |
| `prices[].price` | number |  |
| `prices[].productId` | number |  |
| `tax` | number |  |
| `unit` | string |  |
| `updateTime` | string |  |
| `visibleTo` | number |  |

## Native endpoint

Through the native Pipedrive API, this operation is `POST v2/products` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-product.md) for the provider-specific parameters and requirements.

