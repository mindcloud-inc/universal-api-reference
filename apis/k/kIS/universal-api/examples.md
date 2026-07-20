# KIS Universal API Examples

These examples use the MindCloud API key and KIS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tables

Retrieves all data table structures from KIS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kIS/latest/actions/list-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kIS/latest/actions/list-tables?${params}`, {
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

See the full [List Tables action reference](actions/list-tables.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kIS/latest/actions/list-tables).

## Create Records

Creates one or more records in a KIS data table.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kIS/latest/actions/create-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionName": "Ava Chen",
  "documents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kIS/latest/actions/create-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionName": "Ava Chen",
    "documents[]": [{}]
  })
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

See the full [Create Records action reference](actions/create-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kIS/latest/actions/create-records).
