# NeetoForm: Add Team Members

Adds team members to a NeetoForm workspace.

```
POST https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/add-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/add-team-members" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/add-team-members', {
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
| `organizationRole` | string | no | Role assigned to the new team members in the workspace. |
| `emails[]` | array<string> | yes | Emails of the team members to add to the workspace. |
| `invitedBy` | string | no | Email of the admin sending the invitation. |
| `sendInvitationEmail` | string | no | Set to false to skip sending invitation emails. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native NeetoForm API, this operation is `POST /team_members` (base URL `https://{{credentials.workspaceSubdomain}}.neetoform.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-team-members.md) for the provider-specific parameters and requirements.

