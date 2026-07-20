# SignalZen: Get User

Retrieves a user from SignalZen.

```
GET https://connect.mindcloud.co/v1/universal/signalZen/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalZen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalZen/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalZen/latest/actions/get-user?${params}`, {
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
| `userId` | number | yes | The ID of the user to retrieve. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "last_url": "https://example.com",
      "name": "Ava Chen",
      "online_at": "2026-05-07T12:00:00.000Z",
      "reference": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_attributes": [
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
| `created_at` | date |  |
| `email` | string |  |
| `id` | number |  |
| `last_url` | string |  |
| `name` | string |  |
| `online_at` | date |  |
| `reference` | string |  |
| `updated_at` | date |  |
| `user_attributes` | array<object> |  |

## Native endpoint

Through the native SignalZen API, this operation is `GET /users/{userId}` (base URL `https://api.signalzen.com/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

