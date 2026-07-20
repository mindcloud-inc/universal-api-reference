# Pipio: Generate Dubbed Video V2

Creates a dubbed video in Pipio using the v2 workflow.

```
POST https://connect.mindcloud.co/v1/universal/pipio/latest/actions/generate-dubbed-video-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipio/latest/actions/generate-dubbed-video-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceUrl": "https://cdn.pipio.ai/your-video.mp4",
  "targetLanguage": "es"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipio/latest/actions/generate-dubbed-video-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceUrl": "https://cdn.pipio.ai/your-video.mp4",
    "targetLanguage": "es"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceUrl` | string | yes | The URL to your source video that will be dubbed. Example: `https://cdn.pipio.ai/your-video.mp4`. |
| `targetLanguage` | string | yes | Language code to translate and dub the video into. Default: `es`. Example: `es`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceLanguage` | string | no | Language code of the source video, or auto for automatic detection. Default: `auto`. Example: `auto`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bypassEditing": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bypassEditing` | boolean | Whether the project bypassed manual editing. |
| `id` | string | Generated dubbing project id. |

## Native endpoint

Through the native Pipio API, this operation is `POST https://project.pipio.ai/project/generate/dubbing/v2` (base URL `https://avatar.pipio.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-dubbed-video-v2.md) for the provider-specific parameters and requirements.

