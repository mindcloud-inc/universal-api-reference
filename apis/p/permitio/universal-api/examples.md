# Permit.io Universal API Examples

These examples use the MindCloud API key and Permit.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Key Scope



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-api-key-scope?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-api-key-scope?${params}`, {
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
      "environmentId": "string",
      "organizationId": "string",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get API Key Scope action reference](actions/get-api-key-scope.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/permitio/latest/actions/get-api-key-scope).

## Assign Role



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/assign-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projId": "string",
  "envId": "string",
  "role": "string",
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/permitio/latest/actions/assign-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projId": "string",
    "envId": "string",
    "role": "string",
    "user": "string"
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
      "environmentId": "string",
      "id": "string",
      "organizationId": "string",
      "projectId": "string",
      "resourceInstance": "string",
      "resourceInstanceId": "string",
      "role": "string",
      "roleId": "string",
      "tenant": "string",
      "tenantId": "string",
      "user": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Assign Role action reference](actions/assign-role.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/permitio/latest/actions/assign-role).
