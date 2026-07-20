# Zite Universal API Examples

These examples use the MindCloud API key and Zite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Databases

Retrieves all databases available in Zite.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zite/latest/actions/get-databases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zite/latest/actions/get-databases?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Databases action reference](actions/get-databases.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zite/latest/actions/get-databases).

## Create Database

Creates a new database in Zite.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zite/latest/actions/create-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zite/latest/actions/create-database', {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "tables": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Database action reference](actions/create-database.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zite/latest/actions/create-database).
