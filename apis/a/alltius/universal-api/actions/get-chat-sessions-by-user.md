# Alltius: Get Chat Sessions By User

Retrieves chat sessions for an Alltius user.

```
GET https://connect.mindcloud.co/v1/universal/alltius/latest/actions/get-chat-sessions-by-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alltius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alltius/latest/actions/get-chat-sessions-by-user?connectionId=$CONNECTION_ID&userId=customer-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "customer-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alltius/latest/actions/get-chat-sessions-by-user?${params}`, {
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
| `userId` | string | yes | Example: `customer-123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no |  |
| `pageSize` | number | no | Number of sessions to fetch. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assistant_id": "string",
      "cursor": "string",
      "has_next_page": true,
      "sessions": [
        {}
      ],
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assistant_id` | string | Assistant ID used for the lookup. |
| `cursor` | string | Cursor for the next page. |
| `has_next_page` | boolean | Whether another page is available. |
| `sessions` | array<object> | Matching chat sessions. |
| `user_id` | string | User identifier used for the lookup. |

## Native endpoint

Through the native Alltius API, this operation is `POST /v1/chat/chat_session_by_uid` (base URL `https://app.alltius.ai/api/platform`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-sessions-by-user.md) for the provider-specific parameters and requirements.

