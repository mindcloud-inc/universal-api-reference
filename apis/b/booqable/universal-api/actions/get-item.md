# Booqable: Get Item

Retrieves an item from Booqable.

```
GET https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-item?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-item?${params}`, {
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
| `id` | string | yes | Item ID. |
| `fields.items` | string | no | Comma-separated item fields to include instead of the default field set. |
| `include` | string | no | Comma-separated relationships to sideload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "allowShortage": true,
        "archived": true,
        "basePriceInCents": 1,
        "bufferTimeAfter": 1,
        "bufferTimeBefore": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "defaultPurchaseCostInCents": 1,
        "depositInCents": 1,
        "description": "string",
        "discountable": true,
        "extraInformation": "string",
        "groupName": "Ava Chen",
        "hasVariations": true,
        "name": "Ava Chen",
        "photoId": "string",
        "pricePeriod": "string",
        "priceType": "string",
        "productType": "string",
        "properties": {},
        "shortageLimit": 1,
        "showInStore": true,
        "sku": "string",
        "slug": "string",
        "sortingWeight": 1,
        "tagList": [
          "string"
        ],
        "taxable": true,
        "taxCategoryId": "string",
        "trackable": true,
        "trackingType": "string",
        "type": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "variation": true
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.allowShortage` | boolean | Whether shortage is allowed. |
| `attributes.archived` | boolean | Whether the item is archived. |
| `attributes.basePriceInCents` | number | Base price in cents. |
| `attributes.bufferTimeAfter` | number | Post-rental buffer time. |
| `attributes.bufferTimeBefore` | number | Pre-rental buffer time. |
| `attributes.createdAt` | date | When the item was created. |
| `attributes.defaultPurchaseCostInCents` | number | Default purchase cost in cents. |
| `attributes.depositInCents` | number | Deposit in cents. |
| `attributes.description` | string | Full description. |
| `attributes.discountable` | boolean | Whether discounts are allowed. |
| `attributes.extraInformation` | string | Additional information. |
| `attributes.groupName` | string | Parent group name when applicable. |
| `attributes.hasVariations` | boolean | Whether the item has variations. |
| `attributes.name` | string | Item name. |
| `attributes.photoId` | string | Photo ID. |
| `attributes.pricePeriod` | string | Price period. |
| `attributes.priceType` | string | Price type. |
| `attributes.productType` | string | Product type. |
| `attributes.properties` | object | Custom properties. |
| `attributes.shortageLimit` | number | Shortage limit. |
| `attributes.showInStore` | boolean | Whether the item is visible in the store. |
| `attributes.sku` | string | SKU. |
| `attributes.slug` | string | Store slug. |
| `attributes.sortingWeight` | number | Sorting weight. |
| `attributes.tagList` | array<string> | Item tags. |
| `attributes.taxable` | boolean | Whether the item is taxable. |
| `attributes.taxCategoryId` | string | Tax category ID. |
| `attributes.trackable` | boolean | Whether the item is trackable. |
| `attributes.trackingType` | string | Tracking type. |
| `attributes.type` | string | Underlying item subtype. |
| `attributes.updatedAt` | date | When the item was last updated. |
| `attributes.variation` | boolean | Whether the item is a variation. |
| `id` | string | Item ID. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Booqable API, this operation is `GET /items/:id` (base URL `https://mindcloud.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

