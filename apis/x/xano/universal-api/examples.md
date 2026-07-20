# Xano Universal API Examples

These examples use the MindCloud API key and Xano connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the authenticated user from Xano.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-current-user?${params}`, {
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
      "email": "ava@example.com",
      "extras": {
        "instance": {
          "display": "string",
          "id": 1,
          "name": "Ava Chen"
        }
      },
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xano/latest/actions/get-current-user).

## Create API

Creates a new API endpoint in Xano.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xano/latest/actions/create-api" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "apigroup_id": 1,
  "description": "string",
  "name": "Ava Chen",
  "verb": "string",
  "workspace_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xano/latest/actions/create-api', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "apigroup_id": 1,
    "description": "string",
    "name": "Ava Chen",
    "verb": "string",
    "workspace_id": 1
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
      "auth": true,
      "cache": {
        "active": true,
        "auth": true,
        "datasource": true,
        "input": true,
        "ip": true,
        "ttl": 1
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "docs": "string",
      "guid": "string",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "verb": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create API action reference](actions/create-api.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xano/latest/actions/create-api).
