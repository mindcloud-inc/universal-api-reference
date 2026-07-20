# Dify: Upload File

Uploads a file to Dify.

```
POST https://connect.mindcloud.co/v1/universal/dify/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dify/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dify/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | File to upload. |
| `user` | string | no | User identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversationId": "string",
      "createdAt": 1,
      "createdBy": "string",
      "extension": "string",
      "fileKey": "string",
      "id": "string",
      "mimeType": "string",
      "name": "Ava Chen",
      "originalUrl": "https://example.com",
      "previewUrl": "https://example.com",
      "size": 1,
      "sourceUrl": "https://example.com",
      "tenantId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversationId` | string |  |
| `createdAt` | number |  |
| `createdBy` | string |  |
| `extension` | string |  |
| `fileKey` | string |  |
| `id` | string |  |
| `mimeType` | string |  |
| `name` | string |  |
| `originalUrl` | string |  |
| `previewUrl` | string |  |
| `size` | number |  |
| `sourceUrl` | string |  |
| `tenantId` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Dify API, this operation is `POST /files/upload` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

