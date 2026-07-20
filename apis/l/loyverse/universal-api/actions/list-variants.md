# Loyverse: List Variants

Retrieves product variant records from Loyverse.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-variants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-variants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-variants?${params}`, {
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
| `variantsIds` | string | no | Return only variants specified by a comma-separated list of IDs |
| `itemsIds` | string | no | Return only variants attached to specified item ids |
| `sku` | string | no | Filter variants by sku |
| `createdAtMin` | date | no | Show resources created after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `createdAtMax` | date | no | Show resources created before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updatedAtMin` | string | no | Show resources updated after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updatedAtMax` | string | no | Show resources updated before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `limit` | number | no | Used for pagination |
| `cursor` | string | no | Used for pagination |
| `showDeleted` | boolean | no | Show deleted modifiers and modifier options |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "variants": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `variants` | array<object> |  |
| `variants[].barcode` | string |  |
| `variants[].cost` | number | The variant cost |
| `variants[].createdAt` | date | The time when this resource was created |
| `variants[].defaultPrice` | number | The default variant price (only for `pricing_type: FIXED`) If there are several stores in the account than the price of the variant in each store is equal to this value by default unless different value is specified in the `stores` array for a particular store. |
| `variants[].defaultPricingType` | string | The default variant pricing type. If the value is `VARIABLE` than the price is specified at the time of a sale. If there are several stores in the account than the price of the variant in each store is equal to this value by default unless different value is specified in the `stores` array for a particular store. |
| `variants[].deletedAt` | date | The time when this resource was created |
| `variants[].itemId` | string | The item id this variant is attached to. |
| `variants[].option1Value` | string | The value of the first option for this variant. Required if option1_name is set for the item this variant is attached to. |
| `variants[].option2Value` | string | The value of the second option for this variant. Required if option2_name is set for the item this variant is attached to. |
| `variants[].option3Value` | string | The value of the third option for this variant. Required if option3_name is set for the item this variant is attached to. |
| `variants[].purchaseCost` | number | The variant purchase cost |
| `variants[].referenceVariantId` | string | External reference id for the variant |
| `variants[].sku` | string | The variant sku. It should be unique. |
| `variants[].stores` | array<object> | The list of values that are unique for each store |
| `variants[].stores[].availableForSale` | boolean | If true, variant is available for sale at this store |
| `variants[].stores[].lowStock` | number | The low stock threshold for the variant. If the variant stock is equal or below this threshold, the system shows alert in the back-office and sends email (if enabled). [Learn more](https://help.loyverse.com/help/low-stocks) |
| `variants[].stores[].optimalStock` | number | The variant optimal stock. This value is used to automatically calculate stock while creating purchase order. [Learn more](https://help.loyverse.com/help/autofill-items-purchase-order) |
| `variants[].stores[].price` | number | The variant price in this store (only if pricing_type in this store is `FIXED`). The value is equal to `default_price` by default |
| `variants[].stores[].pricingType` | string | The variant pricing type. If the value is `VARIABLE` than the price is specified at the time of a sale. The value is equal to `default_pricing_type` by default |
| `variants[].stores[].storeId` | string |  |
| `variants[].updatedAt` | date | The time when this resource was created |
| `variants[].variantId` | string | The read only internal id of the variant. |

## Native endpoint

Through the native Loyverse API, this operation is `GET /variants` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-variants.md) for the provider-specific parameters and requirements.

