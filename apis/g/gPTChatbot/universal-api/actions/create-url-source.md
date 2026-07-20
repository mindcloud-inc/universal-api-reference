# GPT Chatbot: Create URL Source

Creates a URL source for a chatbot in GPT Chatbot.

```
POST https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/create-url-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/create-url-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatbotUuid": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/create-url-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatbotUuid": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatbotUuid` | string | yes | Chatbot uuid. |
| `url` | string | yes | Source URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileName": "Ava Chen",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "title": "string",
      "tokensPerChunk": 1,
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
| `createdAt` | date |  |
| `fileName` | string |  |
| `modifiedAt` | date |  |
| `status` | string |  |
| `title` | string |  |
| `tokensPerChunk` | number |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native GPT Chatbot API, this operation is `POST /chatbot/:uuid/data-source/url` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-url-source.md) for the provider-specific parameters and requirements.

