# Farmbrite: Create product

Creates a new product in Farmbrite.

```
POST https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "price": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "price": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes |  |
| `price` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableOnline": true,
      "cartId": "string",
      "category": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deliveryOptions": [
        "string"
      ],
      "description": "string",
      "electronicId": "string",
      "id": "string",
      "increment": 1,
      "isParent": true,
      "minOrder": "string",
      "parentProductId": "string",
      "pinned": true,
      "price": 1,
      "qtyRemaining": "string",
      "sku": "string",
      "status": "string",
      "taxBehavior": "string",
      "taxCode": "string",
      "taxRate": "string",
      "title": "string",
      "transactionCategoryId": "string",
      "type": "string",
      "unitLabel": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "wholesaleOnly": true,
      "wholesalePrice": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableOnline` | boolean |  |
| `cartId` | string |  |
| `category` | string |  |
| `createdAt` | date |  |
| `deliveryOptions` | array<string> |  |
| `description` | string |  |
| `electronicId` | string |  |
| `id` | string |  |
| `increment` | number |  |
| `isParent` | boolean |  |
| `minOrder` | string |  |
| `parentProductId` | string |  |
| `pinned` | boolean |  |
| `price` | number |  |
| `qtyRemaining` | string |  |
| `sku` | string |  |
| `status` | string |  |
| `taxBehavior` | string |  |
| `taxCode` | string |  |
| `taxRate` | string |  |
| `title` | string |  |
| `transactionCategoryId` | string |  |
| `type` | string |  |
| `unitLabel` | string |  |
| `updatedAt` | date |  |
| `wholesaleOnly` | boolean |  |
| `wholesalePrice` | string |  |

## Native endpoint

Through the native Farmbrite API, this operation is `POST /products` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

