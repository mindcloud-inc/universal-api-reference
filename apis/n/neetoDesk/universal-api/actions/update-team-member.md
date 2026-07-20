# NeetoDesk: Update Team Member



```
PUT https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/update-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/update-team-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamMemberId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/update-team-member', {
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
| `teamMemberId` | string | yes | Identifier of the team member. |
| `firstName` | string | no | Updated first name. |
| `lastName` | string | no | Updated last name. |
| `timeZone` | string | no | Updated time zone. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationRole` | string | no | Updated organization role. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NeetoDesk API returns.

## Native endpoint

Through the native NeetoDesk API, this operation is `PATCH /team-members/:team_member_id` (base URL `https://{{credentials.workspaceSubdomain}}.neetodesk.com/api/external/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team-member.md) for the provider-specific parameters and requirements.

