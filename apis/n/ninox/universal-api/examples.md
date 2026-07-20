# Ninox Universal API Examples

These examples use the MindCloud API key and Ninox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download File

Retrieves a file from a Ninox record.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/download-file?connectionId=$CONNECTION_ID&teamId=team_id&dbId=database_id&tableId=A&recordId=1&file=invoice.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "team_id",
  "dbId": "database_id",
  "tableId": "A",
  "recordId": "1",
  "file": "invoice.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/download-file?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Download File action reference](actions/download-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ninox/latest/actions/download-file).

## Create Or Update Records

Creates or updates multiple records in a Ninox table.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/create-or-update-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "YcHTn3ir8XNSp5EXK",
  "dbId": "database_id",
  "tableId": "table_id",
  "records": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninox/latest/actions/create-or-update-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "YcHTn3ir8XNSp5EXK",
    "dbId": "database_id",
    "tableId": "table_id",
    "records": "[object Object]"
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
      "_cd": "string",
      "_cu": "string",
      "_id": 1,
      "_md": "string",
      "_mu": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Or Update Records action reference](actions/create-or-update-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ninox/latest/actions/create-or-update-records).
