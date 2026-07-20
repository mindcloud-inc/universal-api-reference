# Swit: Create Team

Creates a new team in Swit.

```
POST https://connect.mindcloud.co/v1/universal/swit/latest/actions/create-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swit/latest/actions/create-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamName": "Ava Chen",
  "parentId": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swit/latest/actions/create-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamName": "Ava Chen",
    "parentId": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamName` | string | yes | Name of the team to create. |
| `parentId` | number | yes | Parent team ID. Use 0 for a root team. Default: `0`. |
| `reference` | string | no | Optional external reference for the team. |

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

Through the native Swit API, this operation is `POST team.create` (base URL `https://openapi.swit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team.md) for the provider-specific parameters and requirements.

