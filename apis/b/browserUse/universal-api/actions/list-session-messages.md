# Browser Use: List Session Messages

Retrieves session messages from Browser Use.

```
GET https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-session-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-session-messages?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-session-messages?${params}`, {
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
| `after` | string | no | Return messages after this message ID. |
| `before` | string | no | Return messages before this message ID. |
| `sessionId` | string | yes | Browser Use session ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of messages to return, maximum 100. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "messages": [
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
| `hasMore` | boolean |  |
| `messages` | array<object> |  |

## Native endpoint

Through the native Browser Use API, this operation is `GET /sessions/:session_id/messages` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-session-messages.md) for the provider-specific parameters and requirements.

