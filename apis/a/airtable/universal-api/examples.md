# Airtable Universal API Examples

These examples use the MindCloud API key and Airtable connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bases

Retrieves accessible bases from the Airtable account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-bases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-bases?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "permissionLevel": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Bases action reference](actions/list-bases.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airtable/latest/actions/list-bases).

## Create Record

Creates a new record in a specific Airtable table.

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

Example response:

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

See the full [Create Record action reference](actions/create-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airtable/latest/actions/create-record).
