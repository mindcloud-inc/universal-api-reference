# Discourse: Get User

Retrieves a Discourse user by username.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-user?connectionId=$CONNECTION_ID&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-user?${params}`, {
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
      "user": {},
      "user_badges": [
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
| `badge_types` | array<object> |  |
| `badges` | array<object> |  |
| `user` | object |  |
| `user_badges` | array<object> |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /u/:username.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

