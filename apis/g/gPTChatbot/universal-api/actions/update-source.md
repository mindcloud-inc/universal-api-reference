# GPT Chatbot: Update Source

Updates an existing source in GPT Chatbot.

```
PUT https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/update-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/update-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceUuid": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/update-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceUuid": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceUuid` | string | yes | Source uuid. |
| `title` | string | yes | Source title. |

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

Through the native GPT Chatbot API, this operation is `POST /data-source/:uuid/update` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-source.md) for the provider-specific parameters and requirements.

