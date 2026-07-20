# Farmbrite: Retrieve product

Retrieves a specific product from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-product?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/retrieve-product?${params}`, {
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
| `productId` | string | yes |  |

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

Through the native Farmbrite API, this operation is `GET /products/:product_id` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-product.md) for the provider-specific parameters and requirements.

