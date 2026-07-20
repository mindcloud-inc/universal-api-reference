# Alltius: Delete User Chat Sessions

Deletes chat sessions for an Alltius user.

```
DELETE https://connect.mindcloud.co/v1/universal/alltius/latest/actions/delete-user-chat-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alltius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/alltius/latest/actions/delete-user-chat-sessions?connectionId=$CONNECTION_ID&uid=customer-123&sessionIds=session-1%2Csession-2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "customer-123",
  "sessionIds": "session-1,session-2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alltius/latest/actions/delete-user-chat-sessions?${params}`, {
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
| `uid` | string | yes | Example: `customer-123`. |
| `sessionIds` | object | yes | Provide a JSON array of session IDs. Example: `session-1,session-2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the requested sessions were deleted. |

## Native endpoint

Through the native Alltius API, this operation is `POST /v1/chat/delete_chat_sessions_for_uid` (base URL `https://app.alltius.ai/api/platform`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user-chat-sessions.md) for the provider-specific parameters and requirements.

