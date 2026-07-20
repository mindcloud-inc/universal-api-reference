# VdoCipher: Delete Video File

Deletes an existing video file from VdoCipher.

```
DELETE https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/delete-video-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/delete-video-file?connectionId=$CONNECTION_ID&videoId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/delete-video-file?${params}`, {
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
| `videoId` | string | yes |  |
| `fileId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bitrate": 1,
      "enabled": true,
      "format": "string",
      "height": 1,
      "id": "string",
      "isDeletable": true,
      "isDownloadable": true,
      "size": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bitrate` | number |  |
| `enabled` | boolean |  |
| `format` | string |  |
| `height` | number |  |
| `id` | string |  |
| `isDeletable` | boolean |  |
| `isDownloadable` | boolean |  |
| `size` | string |  |
| `width` | number |  |

## Native endpoint

Through the native VdoCipher API, this operation is `DELETE /videos/:videoId/files/:fileId` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-video-file.md) for the provider-specific parameters and requirements.

