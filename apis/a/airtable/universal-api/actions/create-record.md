# Airtable: Create Record

Creates a new record in a specific Airtable table.

```
POST https://connect.mindcloud.co/v1/universal/airtable/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airtable/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "tableId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airtable/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "tableId": "string"
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
| `body` | object | no |  |

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
        "displayPrice": "string",
        "ebayListingStatusLastModifiedTime": "2026-05-07T12:00:00.000Z",
        "fxPictureCount": 1,
        "inventoryCount": 1,
        "inventoryCountLastModifiedTime": "2026-05-07T12:00:00.000Z",
        "inventoryOrDropShip": "string",
        "lastModifiedTime": "2026-05-07T12:00:00.000Z",
        "productLastModifiedTime": "2026-05-07T12:00:00.000Z",
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
| `fields.displayPrice` | string |  |
| `fields.ebayListingStatusLastModifiedTime` | date |  |
| `fields.fxPictureCount` | number |  |
| `fields.inventoryCount` | number |  |
| `fields.inventoryCountLastModifiedTime` | date |  |
| `fields.inventoryOrDropShip` | string |  |
| `fields.lastModifiedTime` | date |  |
| `fields.productLastModifiedTime` | date |  |
| `fields.sku` | string |  |
| `id` | string |  |
| `viewRecord` | string |  |

## Native endpoint

Through the native Airtable API, this operation is `POST /:baseId/:tableId` (base URL `https://api.airtable.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

