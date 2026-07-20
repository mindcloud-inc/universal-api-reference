# JoggAI: Translate Video



```
POST https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/translate-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/translate-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputLanguage": "string",
  "videoUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/translate-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputLanguage": "string",
    "videoUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addSubtitles` | boolean | no | Whether to include subtitles |
| `callbackUrl` | string | no | Webhook callback URL for completion notifications |
| `enableDynamicDuration` | boolean | no | Whether to adapt translated video duration dynamically |
| `outputLanguage` | string | yes | Target language for translation |
| `outputVoice` | string | no | Voice ID for dubbed audio |
| `title` | string | no | Title for the translated video |
| `translateAudioOnly` | boolean | no | Translate audio only without lip sync |
| `videoUrl` | string | yes | URL of the video to translate |

## Response

```json
{
  "success": true,
  "data": [
    {
      "videoTranslateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `videoTranslateId` | string | Created video translation task identifier |

## Native endpoint

Through the native JoggAI API, this operation is `POST /v2/video_translate/` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-video.md) for the provider-specific parameters and requirements.

