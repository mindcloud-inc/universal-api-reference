# VdoCipher: List Video Files

Lists video files in VdoCipher.

```
GET https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/list-video-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/list-video-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/list-video-files?${params}`, {
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

Through the native VdoCipher API, this operation is `GET /videos/:videoId/files` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-video-files.md) for the provider-specific parameters and requirements.

