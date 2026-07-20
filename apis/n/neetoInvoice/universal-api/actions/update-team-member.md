# NeetoInvoice: Update Team Member

Updates an existing team member in NeetoInvoice.

```
PUT https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/update-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoInvoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/update-team-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/update-team-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamMemberId` | string | no | Team member identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "teamMember": {
        "active": true,
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen"
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
| `teamMember.email` | string |  |
| `teamMember.firstName` | string |  |
| `teamMember.id` | string |  |
| `teamMember.lastName` | string |  |

## Native endpoint

Through the native NeetoInvoice API, this operation is `PATCH /team_members/{team_member_id}` (base URL `https://{{credentials.workspaceSubdomain}}.neetoinvoice.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team-member.md) for the provider-specific parameters and requirements.

