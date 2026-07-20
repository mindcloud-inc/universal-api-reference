# Astra Universal API Examples

These examples use the MindCloud API key and Astra connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Org

Retrieves the current organization from Astra.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/astra/latest/actions/get-current-org?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/astra/latest/actions/get-current-org?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Org action reference](actions/get-current-org.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/astra/latest/actions/get-current-org).

## Create Database

Creates a new database in Astra.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/astra/latest/actions/create-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloudProvider": "string",
  "name": "Ava Chen",
  "region": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/astra/latest/actions/create-database', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloudProvider": "string",
    "name": "Ava Chen",
    "region": "string"
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

See the full [Create Database action reference](actions/create-database.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/astra/latest/actions/create-database).
