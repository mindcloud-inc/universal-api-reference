# Walmart: Get Item

Retrieved detailed information about a specific item from the partner's catalog.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-item?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-item?${params}`, {
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
| `id` | string | yes | A unique seller-specified identifier for the item. Defaults to the SKU code. |
| `productIdType` | list<string> | no | Search by additional supported product identifiers (SKU, GTIN, EAN, ISBN, EAN, and Item ID). Use this parameter if you need to filter results based on a specific product ID type. If not specified, the call searches by SKU by default. |
| `condition` | list<string> | no | Indicates the condition of the product. Specify this parameter to filter items based on their condition. |
| `availability` | list<string> | no | Specifies the product's availability status. Use this parameter to filter items by their availability status. |
| `showDuplicateItemDetails` | boolean | no | Toggle on to receive information on duplicate items. |
| `includeCustomerFavoritesStatus` | boolean | no | Toggle on to include `isCustomerFavorite` item details in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": "string",
      "condition": "string",
      "duplicateItemDetails": {
        "destinationItem": {
          "gtin": "string",
          "mart": "string",
          "productName": "Ava Chen",
          "productType": "string",
          "upc": "string",
          "wpid": "string"
        },
        "identifiedDate": "string",
        "lastUpdatedDate": "string",
        "productAttributes": [
          {
            "attributeName": {
              "destinationItemValue": "Ava Chen",
              "sourceItemValue": "Ava Chen"
            }
          }
        ],
        "status": "string"
      },
      "gtin": "string",
      "isCustomerFavorite": "string",
      "isDuplicate": "string",
      "lifecycleStatus": "string",
      "mart": "string",
      "price": {
        "amount": 1,
        "currency": "string"
      },
      "productName": "Ava Chen",
      "productType": "string",
      "publishedStatus": "string",
      "shelf": [
        "string"
      ],
      "sku": "string",
      "upc": "string",
      "wpid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | string |  |
| `condition` | string |  |
| `duplicateItemDetails.destinationItem.gtin` | string |  |
| `duplicateItemDetails.destinationItem.mart` | string |  |
| `duplicateItemDetails.destinationItem.productName` | string |  |
| `duplicateItemDetails.destinationItem.productType` | string |  |
| `duplicateItemDetails.destinationItem.upc` | string |  |
| `duplicateItemDetails.destinationItem.wpid` | string |  |
| `duplicateItemDetails.identifiedDate` | string |  |
| `duplicateItemDetails.lastUpdatedDate` | string |  |
| `duplicateItemDetails.productAttributes[].attributeName.destinationItemValue` | string |  |
| `duplicateItemDetails.productAttributes[].attributeName.sourceItemValue` | string |  |
| `duplicateItemDetails.status` | string |  |
| `gtin` | string |  |
| `isCustomerFavorite` | string |  |
| `isDuplicate` | string |  |
| `lifecycleStatus` | string |  |
| `mart` | string |  |
| `price.amount` | number |  |
| `price.currency` | string |  |
| `productName` | string |  |
| `productType` | string |  |
| `publishedStatus` | string |  |
| `shelf[]` | string |  |
| `sku` | string |  |
| `upc` | string |  |
| `wpid` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/items/:id` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

