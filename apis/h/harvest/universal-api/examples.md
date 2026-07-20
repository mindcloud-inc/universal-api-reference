# Harvest Universal API Examples

These examples use the MindCloud API key and Harvest connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Current User

Retrieves the current user from Harvest.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-current-user?${params}`, {
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
      "accessRoles": [
        "string"
      ],
      "avatarUrl": "https://example.com",
      "calendarIntegrationEnabled": true,
      "calendarIntegrationSource": "string",
      "canCreateProjects": true,
      "costRate": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultHourlyRate": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasAccessToAllFutureProjects": true,
      "id": 1,
      "isActive": true,
      "isContractor": true,
      "lastName": "Chen",
      "permissionsClaims": [
        "string"
      ],
      "roles": [
        "string"
      ],
      "telephone": "string",
      "timezone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "weeklyCapacity": 1
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Current User action reference](actions/retrieve-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/harvest/latest/actions/retrieve-current-user).

## Create Client

Creates a new client in Harvest.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": 1,
      "isActive": true,
      "name": "Ava Chen",
      "statementKey": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/harvest/latest/actions/create-client).
