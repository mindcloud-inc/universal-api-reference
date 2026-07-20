# FlowiseAI: Create Attachment Array

Creates an attachment array for a FlowiseAI chat.

```
POST https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/create-attachment-array
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/create-attachment-array" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatflowId": "string",
  "chatId": "string",
  "files[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/create-attachment-array', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatflowId": "string",
    "chatId": "string",
    "files[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatflowId` | string | yes | Chatflow ID that receives uploaded attachments. |
| `chatId` | string | yes | Chat session ID for the attachments. |
| `files[]` | array<file> | yes | Files to upload as multipart form data. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "mimeType": "string",
      "name": "Ava Chen",
      "size": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `mimeType` | string |  |
| `name` | string |  |
| `size` | string |  |

## Native endpoint

Through the native FlowiseAI API, this operation is `POST /attachments/{chatflowId}/{chatId}` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-attachment-array.md) for the provider-specific parameters and requirements.

