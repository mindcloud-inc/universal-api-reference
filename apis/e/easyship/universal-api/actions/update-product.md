# Easyship: Update Product

Updates an existing product in Easyship.

```
PUT https://connect.mindcloud.co/v1/universal/easyship/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyship/latest/actions/update-product', {
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
| `productId` | string | yes | The Easyship product ID. |
| `identifier` | string | no | SKU for the product. |
| `name` | string | no | Human-readable name of the product. |
| `comments` | string | no | Optional comments for the product. |
| `inputType` | string | no | Product input type. |
| `length` | number | no | Length of the product in centimeters. |
| `width` | number | no | Width of the product in centimeters. |
| `height` | number | no | Height of the product in centimeters. |
| `weight` | number | no | Weight of the product in kilograms. |
| `itemCategoryId` | number | no | Item category ID. |
| `storeId` | string | no | Store ID. |
| `platformProductId` | string | no | Platform product ID. |
| `costPrice` | number | no | Product cost price. |
| `costPriceCurrency` | string | no | Product cost currency. |
| `sellingPrice` | number | no | Product selling price. |
| `sellingPriceCurrency` | string | no | Product selling price currency. |
| `imageUrl` | string | no | Product image URL. |
| `pickLocation` | string | no | Pickup location for the product. |
| `originCountryAlpha2` | string | no | Country where the product is manufactured. |
| `hsCode` | string | no | Harmonized System code for customs. |
| `containsLiquids` | boolean | no | Whether the product contains liquids. |
| `containsBatteryPi966` | boolean | no | Whether the product applies packing instruction 966. |
| `containsBatteryPi967` | boolean | no | Whether the product applies packing instruction 967. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": "string",
      "containsBatteryPi966": true,
      "containsBatteryPi967": true,
      "containsLiquids": true,
      "costPrice": 1,
      "costPriceCurrency": "string",
      "createdAt": "string",
      "height": 1,
      "hsCode": "string",
      "id": "string",
      "identifier": "string",
      "imageUrl": "https://example.com",
      "inputType": "string",
      "itemCategory": {},
      "length": 1,
      "name": "Ava Chen",
      "originCountryAlpha2": "string",
      "pickLocation": "string",
      "platformProductId": "string",
      "sellingPrice": 1,
      "sellingPriceCurrency": "string",
      "storeId": "string",
      "updatedAt": "string",
      "weight": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `containsBatteryPi966` | boolean |  |
| `containsBatteryPi967` | boolean |  |
| `containsLiquids` | boolean |  |
| `costPrice` | number |  |
| `costPriceCurrency` | string |  |
| `createdAt` | string |  |
| `height` | number |  |
| `hsCode` | string |  |
| `id` | string |  |
| `identifier` | string |  |
| `imageUrl` | string |  |
| `inputType` | string |  |
| `itemCategory` | object |  |
| `length` | number |  |
| `name` | string |  |
| `originCountryAlpha2` | string |  |
| `pickLocation` | string |  |
| `platformProductId` | string |  |
| `sellingPrice` | number |  |
| `sellingPriceCurrency` | string |  |
| `storeId` | string |  |
| `updatedAt` | string |  |
| `weight` | number |  |
| `width` | number |  |

## Native endpoint

Through the native Easyship API, this operation is `PATCH /products/:product_id` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

