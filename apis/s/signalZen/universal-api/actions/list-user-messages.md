# SignalZen: List User Messages

Retrieves a user's messages from SignalZen.

```
GET https://connect.mindcloud.co/v1/universal/signalZen/latest/actions/list-user-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalZen `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalZen/latest/actions/list-user-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalZen/latest/actions/list-user-messages?${params}`, {
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
| `userId` | number | yes | The ID of the user whose messages you want to list. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_invitation": true,
      "body": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "file_url": "https://example.com",
      "id": 1,
      "read_by_operator": true,
      "read_by_user": true,
      "sender": {},
      "sender_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_invitation` | boolean |  |
| `body` | string |  |
| `created_at` | date |  |
| `file_url` | string |  |
| `id` | number |  |
| `read_by_operator` | boolean |  |
| `read_by_user` | boolean |  |
| `sender` | object |  |
| `sender_type` | string |  |

## Native endpoint

Through the native SignalZen API, this operation is `GET /users/{userId}/messages` (base URL `https://api.signalzen.com/external`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-messages.md) for the provider-specific parameters and requirements.

