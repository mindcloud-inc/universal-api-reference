# Baserow Universal API Examples

These examples use the MindCloud API key and Baserow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List All Tables

Retrieves all accessible tables from Baserow.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-all-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-all-tables?${params}`, {
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
      "databaseId": 1,
      "id": 1,
      "name": "Ava Chen",
      "order": 1
    }
  ],
  "meta": {}
}
```

See the full [List All Tables action reference](actions/list-all-tables.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/baserow/latest/actions/list-all-tables).

## Batch Create Rows

Creates multiple rows in a Baserow table.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/batch-create-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baserow/latest/actions/batch-create-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": 1
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
      "items": [
        {
          "active": true,
          "id": 1,
          "name": "Ava Chen",
          "order": "string",
          "started": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Batch Create Rows action reference](actions/batch-create-rows.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/baserow/latest/actions/batch-create-rows).
