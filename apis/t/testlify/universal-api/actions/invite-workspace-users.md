# Testlify: Invite Workspace Users

Creates workspace user invitations in Testlify.

```
POST https://connect.mindcloud.co/v1/universal/testlify/latest/actions/invite-workspace-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/invite-workspace-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "members[].email": "ava@example.com",
  "members[].role": "string",
  "members[].userRoleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testlify/latest/actions/invite-workspace-users', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "members[].email": "ava@example.com",
    "members[].role": "string",
    "members[].userRoleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `members[].email` | string | yes | Email address of the invited workspace user. |
| `members[].role` | string | yes | Role to assign to the invited user. |
| `members[].userRoleId` | string | yes | Workspace user role identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Testlify API returns.

## Native endpoint

Through the native Testlify API, this operation is `POST /v1/workspace/invite/user` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-workspace-users.md) for the provider-specific parameters and requirements.

