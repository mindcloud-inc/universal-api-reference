# Airtable: Update Record

Updates a record in a specific Airtable table.

```
PUT https://connect.mindcloud.co/v1/universal/airtable/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airtable/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "tableId": "string",
  "recordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airtable/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "tableId": "string",
    "recordId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseId` | list<string> | yes |  |
| `tableId` | list<string> | yes |  |
| `recordId` | string | yes |  |
| `fields` | object | no |  |

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
        "condition": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "displayPrice": "string",
        "ebayListingStatusLastModifiedTime": "2026-05-07T12:00:00.000Z",
        "fxActiveChannels": "string",
        "fxCleanSKU": "string",
        "fxDescLength": 1,
        "fxDescLengthStatus": "string",
        "fxEbayRequirements": "string",
        "fxEbayTitle": "string",
        "fxEbayTitleLength": "string",
        "fxEbayTitleLengthValue": "string",
        "fxIsEbaySKUMatchingSKU": "string",
        "fxMindCloudStatus": "string",
        "fxModelLength": "string",
        "fxPictureCount": 1,
        "fxPicturesStatus": "string",
        "fxProductTitle": "string",
        "fxProductTitleStatus": "string",
        "fxQBODescLenStatus": "string",
        "fxRecordStatus": "string",
        "fxShouldSyncEbay": "string",
        "fxSKUCount": 1,
        "fxSKUStatus": "string",
        "inventoryCount": 1,
        "inventoryCountLastModifiedTime": "2026-05-07T12:00:00.000Z",
        "inventoryOrDropShip": "string",
        "lastModifiedTime": "2026-05-07T12:00:00.000Z",
        "listingLastModifiedTime": "2026-05-07T12:00:00.000Z",
        "manufacturer": "string",
        "model": "string",
        "modelNumber": "string",
        "picturesLastModifiedTime": "2026-05-07T12:00:00.000Z",
        "pipeDriveFieldsLastModified": "2026-05-07T12:00:00.000Z",
        "pipedriveProductID": "string",
        "pipeDriveStatus": "string",
        "productLastModifiedTime": "2026-05-07T12:00:00.000Z",
        "productName": "Ava Chen",
        "quickBooksFieldsLastModified": "2026-05-07T12:00:00.000Z",
        "quickBooksStatus": "string",
        "shopifyProductStatus": "string",
        "sku": "string"
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
| `fields.condition` | string |  |
| `fields.createdAt` | date |  |
| `fields.displayPrice` | string |  |
| `fields.ebayListingStatusLastModifiedTime` | date |  |
| `fields.fxActiveChannels` | string |  |
| `fields.fxCleanSKU` | string |  |
| `fields.fxDescLength` | number |  |
| `fields.fxDescLengthStatus` | string |  |
| `fields.fxEbayRequirements` | string |  |
| `fields.fxEbayTitle` | string |  |
| `fields.fxEbayTitleLength` | string |  |
| `fields.fxEbayTitleLengthValue` | string |  |
| `fields.fxIsEbaySKUMatchingSKU` | string |  |
| `fields.fxMindCloudStatus` | string |  |
| `fields.fxModelLength` | string |  |
| `fields.fxPictureCount` | number |  |
| `fields.fxPicturesStatus` | string |  |
| `fields.fxProductTitle` | string |  |
| `fields.fxProductTitleStatus` | string |  |
| `fields.fxQBODescLenStatus` | string |  |
| `fields.fxRecordStatus` | string |  |
| `fields.fxShouldSyncEbay` | string |  |
| `fields.fxSKUCount` | number |  |
| `fields.fxSKUStatus` | string |  |
| `fields.inventoryCount` | number |  |
| `fields.inventoryCountLastModifiedTime` | date |  |
| `fields.inventoryOrDropShip` | string |  |
| `fields.lastModifiedTime` | date |  |
| `fields.listingLastModifiedTime` | date |  |
| `fields.manufacturer` | string |  |
| `fields.model` | string |  |
| `fields.modelNumber` | string |  |
| `fields.picturesLastModifiedTime` | date |  |
| `fields.pipeDriveFieldsLastModified` | date |  |
| `fields.pipedriveProductID` | string |  |
| `fields.pipeDriveStatus` | string |  |
| `fields.productLastModifiedTime` | date |  |
| `fields.productName` | string |  |
| `fields.quickBooksFieldsLastModified` | date |  |
| `fields.quickBooksStatus` | string |  |
| `fields.shopifyProductStatus` | string |  |
| `fields.sku` | string |  |
| `id` | string |  |
| `viewRecord` | string |  |

## Native endpoint

Through the native Airtable API, this operation is `PATCH /:baseId/:tableId/:recordId` (base URL `https://api.airtable.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.

