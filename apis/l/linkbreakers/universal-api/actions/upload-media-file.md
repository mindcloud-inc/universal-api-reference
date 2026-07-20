# Linkbreakers: Upload a Media File

Uploads a media file to Linkbreakers.

```
POST https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/upload-media-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/upload-media-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/upload-media-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileData` | string | no | The base64-encoded file data to upload. |
| `fileName` | string | no | The name of the file. |
| `mediaType` | string | no | The type of media being uploaded. |
| `visibility` | string | no | The visibility of the uploaded media. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "media": {
        "createdAt": "string",
        "fileName": "Ava Chen",
        "id": "string",
        "mediaType": "string",
        "mimeType": "string",
        "signedUrl": "https://example.com",
        "size": "string",
        "updatedAt": "string",
        "uploadedBy": "string",
        "visibility": "string",
        "workspaceId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `media` | object | Uploaded media asset. |
| `media.createdAt` | string |  |
| `media.fileName` | string |  |
| `media.id` | string |  |
| `media.mediaType` | string |  |
| `media.mimeType` | string |  |
| `media.signedUrl` | string |  |
| `media.size` | string |  |
| `media.updatedAt` | string |  |
| `media.uploadedBy` | string |  |
| `media.visibility` | string |  |
| `media.workspaceId` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `POST /v1/media` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-media-file.md) for the provider-specific parameters and requirements.

