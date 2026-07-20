# Frontegg: Set Permission Roles

Updates the roles assigned to a permission in Frontegg.

```
PUT https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/set-permission-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/set-permission-roles" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "permissionId": "string",
  "roleIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/set-permission-roles', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "permissionId": "string",
    "roleIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `permissionId` | string | yes | Permission ID. |
| `roleIds[]` | array<string> | yes | Role IDs to assign. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Frontegg API returns.

## Native endpoint

Through the native Frontegg API, this operation is `PUT /identity/resources/permissions/v1/:permissionId/roles` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-permission-roles.md) for the provider-specific parameters and requirements.

