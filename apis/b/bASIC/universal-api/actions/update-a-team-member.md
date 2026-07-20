# BASIC: Update a team member

Updates an existing team member in BASIC.

```
PUT https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/update-a-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/update-a-team-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/update-a-team-member', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "account_id": "string",
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
| `data.role_name` | string |  |
| `data.roles` | string |  |
| `data.team_id` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `PATCH /team/{team_id}/member/{member_id}` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-team-member.md) for the provider-specific parameters and requirements.

