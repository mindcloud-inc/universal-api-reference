# VdoCipher: Upload Video File

Uploads a poster or subtitle file to VdoCipher.

```
POST https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/upload-video-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/upload-video-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/upload-video-file', {
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
| `file` | string | no |  |
| `videoId` | string | no |  |

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

Through the native VdoCipher API, this operation is `POST /videos/:videoId/files` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-video-file.md) for the provider-specific parameters and requirements.

