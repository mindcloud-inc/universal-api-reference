# Swit: List Teams

Retrieves teams and member IDs from Swit.

```
GET https://connect.mindcloud.co/v1/universal/swit/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swit/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swit/latest/actions/list-teams?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Swit API, this operation is `GET user.team.list` (base URL `https://openapi.swit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

