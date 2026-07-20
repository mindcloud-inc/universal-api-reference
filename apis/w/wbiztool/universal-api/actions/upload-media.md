# Wbiztool: Upload Media

Uploads a media file to Wbiztool.

```
POST https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/upload-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/upload-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "media_file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/upload-media', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "media_file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `media_file` | file | yes | Binary media file to upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileExtension": "string",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "fileSizeDisplay": "string",
      "fileType": "string",
      "fileUrl": "https://example.com",
      "id": 1,
      "isImage": true,
      "mimeType": "string",
      "originalFileName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `fileExtension` | string |  |
| `fileName` | string |  |
| `fileSize` | number |  |
| `fileSizeDisplay` | string |  |
| `fileType` | string |  |
| `fileUrl` | string |  |
| `id` | number |  |
| `isImage` | boolean |  |
| `mimeType` | string |  |
| `originalFileName` | string |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /media/upload/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-media.md) for the provider-specific parameters and requirements.

