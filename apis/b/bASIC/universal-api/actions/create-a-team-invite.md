# BASIC: Create a team invite

Creates a team invite in BASIC.

```
POST https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/create-a-team-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/create-a-team-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/create-a-team-invite', {
  method: 'POST',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "account_id": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "email_or_username": "ava@example.com",
        "expires_at": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "role_name": "Ava Chen",
        "roles": "string",
        "team_id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.account_id` | string |  |
| `data.created_at` | date |  |
| `data.email_or_username` | string |  |
| `data.expires_at` | date |  |
| `data.id` | string |  |
| `data.role_name` | string |  |
| `data.roles` | string |  |
| `data.team_id` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `POST /team/{team_id}/invite` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-team-invite.md) for the provider-specific parameters and requirements.

