# PixieBrix Universal API Examples

These examples use the MindCloud API key and PixieBrix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Health Check

Retrieves the PixieBrix API health status.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/health-check?${params}`, {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Health Check action reference](actions/health-check.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pixieBrix/latest/actions/health-check).

## Create Database Record

Creates a database record in PixieBrix, merging by key if needed.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/create-database-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "databasePk": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/create-database-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "databasePk": "string",
    "id": "string"
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "data": {},
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Database Record action reference](actions/create-database-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pixieBrix/latest/actions/create-database-record).
