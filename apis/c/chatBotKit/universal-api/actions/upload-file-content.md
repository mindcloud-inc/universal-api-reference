# ChatBotKit: Upload File Content



```
PUT https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/upload-file-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/upload-file-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/upload-file-content', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | The ID of the file to upload |
| `file` | file | yes | The file to upload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "uploadRequest": {
        "method": "string",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `uploadRequest.method` | string |  |
| `uploadRequest.url` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /file/{fileId}/upload` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-content.md) for the provider-specific parameters and requirements.

