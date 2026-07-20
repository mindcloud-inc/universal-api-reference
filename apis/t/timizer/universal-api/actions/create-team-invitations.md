# Timizer: Create Team Invitations

Creates team invitations and users if needed in Timizer.

```
POST https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-team-invitations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-team-invitations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timizer/latest/actions/create-team-invitations', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | number | yes | ID of the team. |
| `invitations[]` | array<object> | no | Invitation entries to create. |
| `invitations[].email` | string | no | Email address for the invited user. |
| `invitations[].firstName` | string | no | Optional first name. |
| `invitations[].lastName` | string | no | Optional last name. |
| `invitations[].note` | string | no | Invitation note. |
| `invitations[].isExternalUser` | boolean | no | Whether the invited member is external to your main company. |
| `sendEmails` | boolean | no | Whether invitation emails should be sent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | array<object> |  |

## Native endpoint

Through the native Timizer API, this operation is `POST /app/admin-teams/:teamId/invitations` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team-invitations.md) for the provider-specific parameters and requirements.

