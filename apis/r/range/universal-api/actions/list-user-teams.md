# Range: List User Teams

List a user's teams with optional archived and following filters.

```
GET https://connect.mindcloud.co/v1/universal/range/latest/actions/list-user-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Range `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/range/latest/actions/list-user-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/range/latest/actions/list-user-teams?${params}`, {
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
| `includeArchived` | boolean | no | Whether to include archived teams. |
| `includeFollowing` | boolean | no | Whether to include followed teams. |
| `userId` | string | no | The Range user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "relatedTeams": [
        {}
      ],
      "teams": [
        {}
      ],
      "users": [
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
| `relatedTeams` | array<object> |  |
| `teams` | array<object> |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Range API, this operation is `GET /v1/users/:userId/teams` (base URL `https://api.range.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-teams.md) for the provider-specific parameters and requirements.

