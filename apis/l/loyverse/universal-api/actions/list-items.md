# Loyverse: List Items

Retrieves item records from the Loyverse catalog.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-items?${params}`, {
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
| `itemsIds` | string | no | Return only items specified by a comma-separated list of IDs |
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
      "items": [
        {
          "categoryId": "string",
          "color": "string",
          "components": [
            {
              "quantity": 1,
              "variantId": "string"
            }
          ],
          "createdAt": "2026-05-07T12:00:00.000Z",
          "deletedAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "form": "string",
          "handle": "string",
          "id": "string",
          "imageUrl": "https://example.com",
          "isComposite": true,
          "itemName": "Ava Chen",
          "modifiersIds": [
            "string"
          ],
          "option1Name": "Ava Chen",
          "option2Name": "Ava Chen",
          "option3Name": "Ava Chen",
          "primarySupplierId": "string",
          "referenceId": "string",
          "soldByWeight": true,
          "taxIds": [
            "string"
          ],
          "trackStock": true,
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "useProduction": true,
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
| `items` | array<object> |  |
| `items[].categoryId` | string | The category id of the item |
| `items[].color` | string | One of the predefined colors for the item that is displayed on the POS |
| `items[].components` | array<object> | The list of components for the item. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `items[].components[].quantity` | number |  |
| `items[].components[].variantId` | string |  |
| `items[].createdAt` | date | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `items[].deletedAt` | date | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `items[].description` | string | The item description. |
| `items[].form` | string | The visual form of the item that is displayed on the POS |
| `items[].handle` | string |  |
| `items[].id` | string | Read-only internal id of the item. If included in the POST request it will cause an update instead of a creating a new object. |
| `items[].imageUrl` | string |  |
| `items[].isComposite` | boolean | If true, the item contains a specified quantity of other items. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `items[].itemName` | string | The item name. |
| `items[].modifiersIds` | array<string> | The list of modifiers ids applied to this item |
| `items[].option1Name` | string | The name of the first option (for example "Size"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `items[].option2Name` | string | The name of the first option (for example "Color"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `items[].option3Name` | string | The name of the first option (for example "Material"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `items[].primarySupplierId` | string |  |
| `items[].referenceId` | string | External reference id for the item |
| `items[].soldByWeight` | boolean | If true, a fractional quantity for this item can be specified at the time of a sale (for example 1.5) |
| `items[].taxIds` | array<string> | The list of tax ids applied to this item |
| `items[].trackStock` | boolean | If true, the system tracks inventory for this item at all stores. Make sure you don't accidentally disable track stock. If you set `track_stock` to false then all inventory levels of this item are set to 0 |
| `items[].updatedAt` | date | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `items[].useProduction` | boolean | If true, the system tracks stock not only for its components but also for this item. This property can be set only for composite items. [Learn more](https://help.loyverse.com/help/how-work-production) |
| `items[].variants` | array<object> |  |
| `items[].variants[].barcode` | string |  |
| `items[].variants[].cost` | number | The variant cost |
| `items[].variants[].createdAt` | date | The time when this resource was created |
| `items[].variants[].defaultPrice` | number | The default variant price (only for `pricing_type: FIXED`) If there are several stores in the account than the price of the variant in each store is equal to this value by default unless different value is specified in the `stores` array for a particular store. |
| `items[].variants[].defaultPricingType` | string | The default variant pricing type. If the value is `VARIABLE` than the price is specified at the time of a sale. If there are several stores in the account than the price of the variant in each store is equal to this value by default unless different value is specified in the `stores` array for a particular store. |
| `items[].variants[].deletedAt` | date | The time when this resource was created |
| `items[].variants[].itemId` | string | The item id this variant is attached to. |
| `items[].variants[].option1Value` | string | The value of the first option for this variant. Required if option1_name is set for the item this variant is attached to. |
| `items[].variants[].option2Value` | string | The value of the second option for this variant. Required if option2_name is set for the item this variant is attached to. |
| `items[].variants[].option3Value` | string | The value of the third option for this variant. Required if option3_name is set for the item this variant is attached to. |
| `items[].variants[].purchaseCost` | number | The variant purchase cost |
| `items[].variants[].referenceVariantId` | string | External reference id for the variant |
| `items[].variants[].sku` | string | The variant sku. It should be unique. |
| `items[].variants[].stores` | array<object> | The list of values that are unique for each store |
| `items[].variants[].stores[].availableForSale` | boolean | If true, variant is available for sale at this store |
| `items[].variants[].stores[].lowStock` | number | The low stock threshold for the variant. If the variant stock is equal or below this threshold, the system shows alert in the back-office and sends email (if enabled). [Learn more](https://help.loyverse.com/help/low-stocks) |
| `items[].variants[].stores[].optimalStock` | number | The variant optimal stock. This value is used to automatically calculate stock while creating purchase order. [Learn more](https://help.loyverse.com/help/autofill-items-purchase-order) |
| `items[].variants[].stores[].price` | number | The variant price in this store (only if pricing_type in this store is `FIXED`). The value is equal to `default_price` by default |
| `items[].variants[].stores[].pricingType` | string | The variant pricing type. If the value is `VARIABLE` than the price is specified at the time of a sale. The value is equal to `default_pricing_type` by default |
| `items[].variants[].stores[].storeId` | string |  |
| `items[].variants[].updatedAt` | date | The time when this resource was created |
| `items[].variants[].variantId` | string | The read only internal id of the variant. |

## Native endpoint

Through the native Loyverse API, this operation is `GET /items` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

