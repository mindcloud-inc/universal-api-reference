# Loyverse: Get Variant

Retrieves a product variant from Loyverse.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-variant?connectionId=$CONNECTION_ID&variantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-variant?${params}`, {
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
| `variantId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "barcode": "string",
      "cost": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultPrice": 1,
      "defaultPricingType": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "itemId": "string",
      "option1Value": "string",
      "option2Value": "string",
      "option3Value": "string",
      "purchaseCost": 1,
      "referenceVariantId": "string",
      "sku": "string",
      "stores": [
        {
          "availableForSale": true,
          "lowStock": 1,
          "optimalStock": 1,
          "price": 1,
          "pricingType": "string",
          "storeId": "string"
        }
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "variantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barcode` | string |  |
| `cost` | number | The variant cost |
| `createdAt` | date | The time when this resource was created |
| `defaultPrice` | number | The default variant price (only for `pricing_type: FIXED`) If there are several stores in the account than the price of the variant in each store is equal to this value by default unless different value is specified in the `stores` array for a particular store. |
| `defaultPricingType` | string | The default variant pricing type. If the value is `VARIABLE` than the price is specified at the time of a sale. If there are several stores in the account than the price of the variant in each store is equal to this value by default unless different value is specified in the `stores` array for a particular store. |
| `deletedAt` | date | The time when this resource was created |
| `itemId` | string | The item id this variant is attached to. |
| `option1Value` | string | The value of the first option for this variant. Required if option1_name is set for the item this variant is attached to. |
| `option2Value` | string | The value of the second option for this variant. Required if option2_name is set for the item this variant is attached to. |
| `option3Value` | string | The value of the third option for this variant. Required if option3_name is set for the item this variant is attached to. |
| `purchaseCost` | number | The variant purchase cost |
| `referenceVariantId` | string | External reference id for the variant |
| `sku` | string | The variant sku. It should be unique. |
| `stores` | array<object> | The list of values that are unique for each store |
| `stores[].availableForSale` | boolean | If true, variant is available for sale at this store |
| `stores[].lowStock` | number | The low stock threshold for the variant. If the variant stock is equal or below this threshold, the system shows alert in the back-office and sends email (if enabled). [Learn more](https://help.loyverse.com/help/low-stocks) |
| `stores[].optimalStock` | number | The variant optimal stock. This value is used to automatically calculate stock while creating purchase order. [Learn more](https://help.loyverse.com/help/autofill-items-purchase-order) |
| `stores[].price` | number | The variant price in this store (only if pricing_type in this store is `FIXED`). The value is equal to `default_price` by default |
| `stores[].pricingType` | string | The variant pricing type. If the value is `VARIABLE` than the price is specified at the time of a sale. The value is equal to `default_pricing_type` by default |
| `stores[].storeId` | string |  |
| `updatedAt` | date | The time when this resource was created |
| `variantId` | string | The read only internal id of the variant. |

## Native endpoint

Through the native Loyverse API, this operation is `GET /variants/:variant_id` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variant.md) for the provider-specific parameters and requirements.

