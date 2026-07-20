# Alltius: Get Chat History

Retrieves chat history for an Alltius session.

```
GET https://connect.mindcloud.co/v1/universal/alltius/latest/actions/get-chat-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alltius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alltius/latest/actions/get-chat-history?connectionId=$CONNECTION_ID&sessionId=a2df6e07-65e1-49e8-945a-f18ac61db234" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "a2df6e07-65e1-49e8-945a-f18ac61db234"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alltius/latest/actions/get-chat-history?${params}`, {
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
| `sessionId` | string | yes | Example: `a2df6e07-65e1-49e8-945a-f18ac61db234`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no |  |
| `pageSize` | number | no | Number of messages to fetch. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chat_history": [
        {}
      ],
      "cursor": "string",
      "has_next_page": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chat_history` | array<object> | Messages in the session. |
| `cursor` | string | Cursor for the next page. |
| `has_next_page` | boolean | Whether another page is available. |

## Native endpoint

Through the native Alltius API, this operation is `POST /v1/chat/history` (base URL `https://app.alltius.ai/api/platform`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-history.md) for the provider-specific parameters and requirements.

