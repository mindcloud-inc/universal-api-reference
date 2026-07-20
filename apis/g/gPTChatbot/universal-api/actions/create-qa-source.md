# GPT Chatbot: Create QA Source

Creates a QA source for a chatbot in GPT Chatbot.

```
POST https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/create-qa-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/create-qa-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "answer": "string",
  "chatbotUuid": "string",
  "question": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/create-qa-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "answer": "string",
    "chatbotUuid": "string",
    "question": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `answer` | string | yes | Answer text. |
| `chatbotUuid` | string | yes | Chatbot uuid. |
| `question` | string | yes | Question text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileName": "Ava Chen",
      "status": "string",
      "title": "string",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileName` | string |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native GPT Chatbot API, this operation is `POST /chatbot/:uuid/data-source/qa` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-qa-source.md) for the provider-specific parameters and requirements.

