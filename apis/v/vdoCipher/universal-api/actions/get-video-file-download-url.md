# VdoCipher: Get Video File Download Url

Retrieves a video file download URL from VdoCipher.

```
GET https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/get-video-file-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/get-video-file-download-url?connectionId=$CONNECTION_ID&videoId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/get-video-file-download-url?${params}`, {
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
      "redirect": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `redirect` | string | URL which is valid for 15 minutes. |

## Native endpoint

Through the native VdoCipher API, this operation is `GET /videos/:videoId/files/:fileId` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-file-download-url.md) for the provider-specific parameters and requirements.

