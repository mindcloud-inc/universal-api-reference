# LoginRadius: Assign Roles in Organization

Updates a user's organization roles in LoginRadius.

```
PUT https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/assign-roles-in-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/assign-roles-in-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orgId": "string",
  "roleId": "string",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/assign-roles-in-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orgId": "string",
    "roleId": "string",
    "uid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orgId` | string | yes | Organization ID in which to assign roles. |
| `roleId` | string | yes | Role ID to assign within the organization. |
| `uid` | string | yes | UID of the user to assign roles to. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LoginRadius API returns.

## Native endpoint

Through the native LoginRadius API, this operation is `PUT /v2/manage/account/:uid/orgcontext/:orgId/roles` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-roles-in-organization.md) for the provider-specific parameters and requirements.

