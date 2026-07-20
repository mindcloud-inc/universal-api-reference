# Discourse: List User Badges

Retrieves badges for a Discourse user.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-user-badges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-user-badges?connectionId=$CONNECTION_ID&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-user-badges?${params}`, {
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
| `username` | string | yes | Discourse username. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badge_types": [
        {}
      ],
      "badges": [
        {}
      ],
      "granted_bies": [
        {}
      ],
      "user_badges": [
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
| `badge_types` | array<object> |  |
| `badges` | array<object> |  |
| `granted_bies` | array<object> |  |
| `user_badges` | array<object> |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /user-badges/:username.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-badges.md) for the provider-specific parameters and requirements.

