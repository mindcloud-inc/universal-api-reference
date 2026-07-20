# Data Blaze Universal API Examples

These examples use the MindCloud API key and Data Blaze connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Table Rows

Retrieves table rows from Data Blaze.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-table-rows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-table-rows?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Table Rows action reference](actions/list-table-rows.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataBlaze/latest/actions/list-table-rows).

## Create Table Row

Creates a new table row in Data Blaze.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/create-table-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Jane Doe"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/create-table-row', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Jane Doe"
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
      "field_028bLj7zLab3TYslzthhXu": "string",
      "field_2Te3k3Sf4edLQ3a0WE2a8J": "string",
      "id": "string",
      "order": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Table Row action reference](actions/create-table-row.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataBlaze/latest/actions/create-table-row).
