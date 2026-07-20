# Airtable: Get Record

Retrieves a specific record from an Airtable table.

```
GET https://connect.mindcloud.co/v1/universal/airtable/latest/actions/get-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airtable/latest/actions/get-record?connectionId=$CONNECTION_ID&baseId=string&tableId=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseId": "string",
  "tableId": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airtable/latest/actions/get-record?${params}`, {
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
| `baseId` | list<string> | yes | To get this value, check this doc https://airtable.com/developers/web/api/list-bases |
| `tableId` | list<string> | yes |  |
| `recordId` | string | yes | The ID of the Airtable Record to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "fields": {
        "addToShopify": {
          "label": "string",
          "url": "https://example.com"
        },
        "category1": "string",
        "condition": "string",
        "cost": 1,
        "displayPrice": "string",
        "ebayListingStatusLastModifiedTime": "2026-05-07T12:00:00.000Z",
        "fxPictureCount": 1,
        "hTMLDescription": "string",
        "inventoryCount": 1,
        "inventoryCountLastModifiedTime": "2026-05-07T12:00:00.000Z",
        "inventoryOrDropShip": "string",
        "lastModifiedTime": "2026-05-07T12:00:00.000Z",
        "listingLastModifiedTime": "2026-05-07T12:00:00.000Z",
        "manufacturer": "string",
        "model": "string",
        "modelNumber": "string",
        "productLastModifiedTime": "2026-05-07T12:00:00.000Z",
        "quickbooksDescription": "string",
        "sellingPrice": 1,
        "shelfLocation": "string",
        "shopifyInventoryItemID": "string",
        "shopifyProductID": "string",
        "shopifyProductStatus": "string",
        "shopifyVariantID": "string",
        "sku": "string",
        "sKUInShopify": true,
        "vendor": "string",
        "warehouseLocation": "string"
      },
      "id": "string",
      "viewRecord": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date |  |
| `fields.addToShopify.label` | string |  |
| `fields.addToShopify.url` | string |  |
| `fields.category1` | string |  |
| `fields.condition` | string |  |
| `fields.cost` | number |  |
| `fields.displayPrice` | string |  |
| `fields.ebayListingStatusLastModifiedTime` | date |  |
| `fields.fxPictureCount` | number |  |
| `fields.hTMLDescription` | string |  |
| `fields.inventoryCount` | number |  |
| `fields.inventoryCountLastModifiedTime` | date |  |
| `fields.inventoryOrDropShip` | string |  |
| `fields.lastModifiedTime` | date |  |
| `fields.listingLastModifiedTime` | date |  |
| `fields.manufacturer` | string |  |
| `fields.model` | string |  |
| `fields.modelNumber` | string |  |
| `fields.productLastModifiedTime` | date |  |
| `fields.quickbooksDescription` | string |  |
| `fields.sellingPrice` | number |  |
| `fields.shelfLocation` | string |  |
| `fields.shopifyInventoryItemID` | string |  |
| `fields.shopifyProductID` | string |  |
| `fields.shopifyProductStatus` | string |  |
| `fields.shopifyVariantID` | string |  |
| `fields.sku` | string |  |
| `fields.sKUInShopify` | boolean |  |
| `fields.vendor` | string |  |
| `fields.warehouseLocation` | string |  |
| `id` | string |  |
| `viewRecord` | string |  |

## Native endpoint

Through the native Airtable API, this operation is `GET /:baseId/:tableId/:recordId` (base URL `https://api.airtable.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record.md) for the provider-specific parameters and requirements.

