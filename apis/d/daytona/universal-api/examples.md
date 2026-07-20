# Daytona Universal API Examples

These examples use the MindCloud API key and Daytona connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current API Key

Retrieves the current API key details from Daytona.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-current-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-current-api-key?${params}`, {
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
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "lastUsedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "permissions": [
        "string"
      ],
      "userId": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current API Key action reference](actions/get-current-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/daytona/latest/actions/get-current-api-key).

## Archive Sandbox

Archives a sandbox in Daytona.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/archive-sandbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sandboxIdOrName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/daytona/latest/actions/archive-sandbox', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sandboxIdOrName": "Ava Chen"
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
      "autoStopInterval": 1,
      "cpu": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "desiredState": "string",
      "disk": 1,
      "env": {},
      "gpu": 1,
      "id": "string",
      "labels": {},
      "memory": 1,
      "name": "Ava Chen",
      "networkBlockAll": true,
      "organizationId": "string",
      "public": true,
      "runnerId": "string",
      "snapshot": "string",
      "state": "string",
      "target": "string",
      "toolboxProxyUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": "string"
    }
  ],
  "meta": {}
}
```

See the full [Archive Sandbox action reference](actions/archive-sandbox.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/daytona/latest/actions/archive-sandbox).
