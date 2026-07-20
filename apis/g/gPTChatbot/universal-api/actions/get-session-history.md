# GPT Chatbot: Get Session History

Retrieves a session's plain-text chat history from GPT Chatbot.

```
GET https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/get-session-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/get-session-history?connectionId=$CONNECTION_ID&sessionUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/get-session-history?${params}`, {
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
| `sessionUuid` | string | yes | Session uuid. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "transcript": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `transcript` | string |  |

## Native endpoint

Through the native GPT Chatbot API, this operation is `GET /session/:uuid/messages/plain-text` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-history.md) for the provider-specific parameters and requirements.

