# NeetoDesk: Add Team Members



```
POST https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/add-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/add-team-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/add-team-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | yes | Emails of the team members to add. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationRole` | string | no | Role assigned to the new team members. |
| `invitedBy` | string | no | Email of the admin sending the invitation. |
| `sendInvitationEmail` | string | no | Whether invitation emails should be sent. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NeetoDesk API returns.

## Native endpoint

Through the native NeetoDesk API, this operation is `POST /team-members` (base URL `https://{{credentials.workspaceSubdomain}}.neetodesk.com/api/external/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-team-members.md) for the provider-specific parameters and requirements.

