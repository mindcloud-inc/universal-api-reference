# NeetoForm: Update Team Member

Updates an existing team member in NeetoForm.

```
PUT https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/update-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/update-team-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamMemberId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/update-team-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamMemberId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamMemberId` | string | yes | ID of the team member you want to update. |
| `email` | string | no | Email of the team member. |
| `firstName` | string | no | First name of the team member. |
| `lastName` | string | no | Last name of the team member. |
| `timeZone` | string | no | Time zone for the team member. |
| `organizationRole` | string | no | Organization role for the team member. This value is case sensitive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "teamMember": {
        "active": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "organizationRole": "string",
        "timeZone": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `teamMember.active` | boolean |  |
| `teamMember.createdAt` | date |  |
| `teamMember.email` | string |  |
| `teamMember.firstName` | string |  |
| `teamMember.id` | string |  |
| `teamMember.lastName` | string |  |
| `teamMember.organizationRole` | string |  |
| `teamMember.timeZone` | string |  |
| `teamMember.updatedAt` | date |  |

## Native endpoint

Through the native NeetoForm API, this operation is `PATCH /team_members/:team_member_id` (base URL `https://{{credentials.workspaceSubdomain}}.neetoform.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team-member.md) for the provider-specific parameters and requirements.

