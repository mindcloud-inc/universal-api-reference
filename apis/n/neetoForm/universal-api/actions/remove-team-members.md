# NeetoForm: Remove Team Members



```
DELETE https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/remove-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/remove-team-members?connectionId=$CONNECTION_ID&emails%5B%5D=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emails[]": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/remove-team-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | yes | Emails of the team members to remove from the workspace. |

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

Through the native NeetoForm API, this operation is `DELETE /team_members` (base URL `https://{{credentials.workspaceSubdomain}}.neetoform.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-team-members.md) for the provider-specific parameters and requirements.

