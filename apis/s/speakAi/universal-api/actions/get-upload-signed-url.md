# Speak Ai: Get Upload Signed URL

Retrieves an upload signed URL from Speak Ai.

```
GET https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-upload-signed-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-upload-signed-url?connectionId=$CONNECTION_ID&isVideo=false&filename=Ava%20Chen&mimeType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "isVideo": "false",
  "filename": "Ava Chen",
  "mimeType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-upload-signed-url?${params}`, {
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
| `isVideo` | boolean | yes | Whether the upload target is a video file instead of audio. Default: `false`. |
| `filename` | string | yes | Filename including the extension for the signed upload target. |
| `mimeType` | string | yes | File MIME type such as audio/mp3 or video/mp4. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "preSignedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string |  |
| `preSignedUrl` | string |  |

## Native endpoint

Through the native Speak Ai API, this operation is `GET /media/upload/signedurl` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload-signed-url.md) for the provider-specific parameters and requirements.

