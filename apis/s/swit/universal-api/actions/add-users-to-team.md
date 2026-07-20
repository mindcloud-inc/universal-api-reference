# Swit: Add Users To Team

Adds users to a team in Swit.

```
PUT https://connect.mindcloud.co/v1/universal/swit/latest/actions/add-users-to-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/swit/latest/actions/add-users-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "userIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swit/latest/actions/add-users-to-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "userIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Target team ID. |
| `userIds[]` | array<string> | yes | List of user IDs to add to the team. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "depth": 1,
      "member_cnt": 1,
      "parent_id": "string",
      "reference": "string",
      "team_id": "string",
      "team_name": "Ava Chen",
      "users": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `depth` | number |  |
| `member_cnt` | number |  |
| `parent_id` | string |  |
| `reference` | string |  |
| `team_id` | string |  |
| `team_name` | string |  |
| `users[]` | array<string> |  |

## Native endpoint

Through the native Swit API, this operation is `POST team.user.add` (base URL `https://openapi.swit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-users-to-team.md) for the provider-specific parameters and requirements.

