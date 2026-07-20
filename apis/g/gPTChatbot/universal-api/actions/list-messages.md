# GPT Chatbot: List Messages

Retrieves messages for a session in GPT Chatbot.

```
GET https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-messages?connectionId=$CONNECTION_ID&sessionUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-messages?${params}`, {
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
      "backgroundPendingTasks": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "errorMessage": "string",
      "finishReason": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "query": "string",
      "response": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backgroundPendingTasks` | number |  |
| `createdAt` | date |  |
| `errorMessage` | string |  |
| `finishReason` | string |  |
| `modifiedAt` | date |  |
| `query` | string |  |
| `response` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native GPT Chatbot API, this operation is `GET /session/:uuid/messages` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

