# GPT Chatbot: Upload File

Uploads a file as a source for a chatbot in GPT Chatbot.

```
POST https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatbotUuid": "string",
  "filePath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatbotUuid": "string",
    "filePath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatbotUuid` | string | yes | Chatbot uuid. |
| `filePath` | file | yes | File uploaded as multipart form-data. |
| `referenceSourceLink` | string | no | Reference source link for the uploaded file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileName": "Ava Chen",
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
| `fileName` | string |  |
| `status` | string |  |
| `title` | string |  |
| `tokensPerChunk` | number |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native GPT Chatbot API, this operation is `POST /chatbot/:uuid/data-source/upload` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

