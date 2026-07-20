# Loyverse: Create or Update Item

Creates or updates an item in Loyverse.

```
PUT https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/create-or-update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/create-or-update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/create-or-update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Read-only internal id of the item. If included in the POST request it will cause an update instead of a creating a new object. |
| `handle` | string | no |  |
| `itemName` | string | yes | The item name. |
| `description` | string | no | The item description. |
| `referenceId` | string | no | External reference id for the item |
| `categoryId` | string | no | The category id of the item |
| `trackStock` | boolean | no | If true, the system tracks inventory for this item at all stores. Make sure you don't accidentally disable track stock. If you set `track_stock` to false then all inventory levels of this item are set to 0 |
| `soldByWeight` | boolean | no | If true, a fractional quantity for this item can be specified at the time of a sale (for example 1.5) |
| `isComposite` | boolean | no | If true, the item contains a specified quantity of other items. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `useProduction` | boolean | no | If true, the system tracks stock not only for its components but also for this item. This property can be set only for composite items. [Learn more](https://help.loyverse.com/help/how-work-production) |
| `components[]` | array<object> | no | The list of components for the item. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `components[]` | array<object> | no | The list of components for the item. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `components[]` | array<object> | no | The list of components for the item. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `primarySupplierId` | string | no |  |
| `taxIds[]` | array<string> | no | The list of tax ids applied to this item |
| `taxIds[]` | array<string> | no | The list of tax ids applied to this item |
| `taxIds[]` | array<string> | no | The list of tax ids applied to this item |
| `modifiersIds[]` | array<string> | no | The list of modifiers ids applied to this item |
| `modifiersIds[]` | array<string> | no | The list of modifiers ids applied to this item |
| `modifiersIds[]` | array<string> | no | The list of modifiers ids applied to this item |
| `form` | string | no | The visual form of the item that is displayed on the POS |
| `color` | string | no | One of the predefined colors for the item that is displayed on the POS |
| `imageUrl` | string | no |  |
| `option1Name` | string | no | The name of the first option (for example "Size"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `option2Name` | string | no | The name of the first option (for example "Color"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `option3Name` | string | no | The name of the first option (for example "Material"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `createdAt` | date | no | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `updatedAt` | date | no | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `deletedAt` | date | no | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `variants[]` | array<object> | no |  |
| `variants[]` | array<object> | no |  |
| `variants[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | string | The category id of the item |
| `color` | string | One of the predefined colors for the item that is displayed on the POS |
| `components` | array<object> | The list of components for the item. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `components[].quantity` | number |  |
| `components[].variantId` | string |  |
| `createdAt` | date | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `deletedAt` | date | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `description` | string | The item description. |
| `form` | string | The visual form of the item that is displayed on the POS |
| `handle` | string |  |
| `id` | string | Read-only internal id of the item. If included in the POST request it will cause an update instead of a creating a new object. |
| `imageUrl` | string |  |
| `isComposite` | boolean | If true, the item contains a specified quantity of other items. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `itemName` | string | The item name. |
| `modifiersIds` | array<string> | The list of modifiers ids applied to this item |
| `option1Name` | string | The name of the first option (for example "Size"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `option2Name` | string | The name of the first option (for example "Color"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `option3Name` | string | The name of the first option (for example "Material"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `primarySupplierId` | string |  |
| `referenceId` | string | External reference id for the item |
| `soldByWeight` | boolean | If true, a fractional quantity for this item can be specified at the time of a sale (for example 1.5) |
| `taxIds` | array<string> | The list of tax ids applied to this item |
| `trackStock` | boolean | If true, the system tracks inventory for this item at all stores. Make sure you don't accidentally disable track stock. If you set `track_stock` to false then all inventory levels of this item are set to 0 |
| `updatedAt` | date | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `useProduction` | boolean | If true, the system tracks stock not only for its components but also for this item. This property can be set only for composite items. [Learn more](https://help.loyverse.com/help/how-work-production) |
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

Through the native Loyverse API, this operation is `POST /items` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-item.md) for the provider-specific parameters and requirements.

