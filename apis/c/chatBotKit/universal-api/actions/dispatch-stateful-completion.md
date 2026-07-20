# ChatBotKit: Dispatch Stateful Completion



```
POST https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/dispatch-stateful-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/dispatch-stateful-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/dispatch-stateful-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | The ID of the conversation to dispatch |
| `text` | string | yes | Text to dispatch for completion |
| `entities[]` | array | no | Entities attached to the dispatched message |
| `functions[]` | array | no | Functions available during dispatch |
| `extensions` | object | no | Extensions for the dispatch request |
| `limits` | object | no | Execution limits for the dispatch request |
| `channelId` | string | no | Channel ID to dispatch the completion to |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /conversation/{conversationId}/dispatch` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dispatch-stateful-completion.md) for the provider-specific parameters and requirements.

