# GPT Chatbot: List Sources

Retrieves sources for a chatbot in GPT Chatbot.

```
GET https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-sources?connectionId=$CONNECTION_ID&chatbotUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatbotUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-sources?${params}`, {
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
| `chatbotUuid` | string | yes | Chatbot uuid. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "metaJson": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "title": "string",
      "tokens": 1,
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
| `fileSize` | number |  |
| `metaJson` | string |  |
| `modifiedAt` | date |  |
| `status` | string |  |
| `title` | string |  |
| `tokens` | number |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native GPT Chatbot API, this operation is `GET /chatbot/:uuid/data-sources` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sources.md) for the provider-specific parameters and requirements.

