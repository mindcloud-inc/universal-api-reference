# LessonBuddy: Get Price By SKU

Retrieves a product price in LessonBuddy by SKU.

```
GET https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-price-by-sku
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LessonBuddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-price-by-sku?connectionId=$CONNECTION_ID&locationId=1&sku=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "1",
  "sku": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/get-price-by-sku?${params}`, {
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
| `locationId` | number | yes | LessonBuddy location ID. |
| `sku` | string | yes | Inventory SKU. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inventoryId": 1,
      "isDiscountable": true,
      "isReturnable": true,
      "isTaxable": true,
      "isVirtual": true,
      "locationId": 1,
      "masterName": "Ava Chen",
      "price": 1,
      "productId": 1,
      "productName": "Ava Chen",
      "productSku": "string",
      "taxRate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventoryId` | number |  |
| `isDiscountable` | boolean |  |
| `isReturnable` | boolean |  |
| `isTaxable` | boolean |  |
| `isVirtual` | boolean |  |
| `locationId` | number |  |
| `masterName` | string |  |
| `price` | number |  |
| `productId` | number |  |
| `productName` | string |  |
| `productSku` | string |  |
| `taxRate` | number |  |

## Native endpoint

Through the native LessonBuddy API, this operation is `GET /v2/ims/inventory/:locationId/price-by-sku/:sku` (base URL `https://api.lessonbuddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-price-by-sku.md) for the provider-specific parameters and requirements.

