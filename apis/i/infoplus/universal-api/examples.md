# Infoplus Universal API Examples

These examples use the MindCloud API key and Infoplus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Items

Finds matching items in Infoplus.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/search-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/search-items?${params}`, {
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
      "createDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "itemDescription": "string",
      "modifyDate": "2026-05-07T12:00:00.000Z",
      "sku": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Items action reference](actions/search-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/infoplus/latest/actions/search-items).

## Create Aisle

Creates a new aisle in Infoplus.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/create-aisle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/create-aisle', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "address": "string",
      "createDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "modifyDate": "2026-05-07T12:00:00.000Z",
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Aisle action reference](actions/create-aisle.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/infoplus/latest/actions/create-aisle).
