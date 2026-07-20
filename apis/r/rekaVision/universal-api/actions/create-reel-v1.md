# Reka Vision: Create Reel (V1)

Creates highlight reels in Reka Vision.

```
POST https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/create-reel-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/create-reel-v1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/create-reel-v1', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoUrls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoUrls[]` | array<string> | yes |  |
| `prompt` | string | no |  |
| `generationConfig.template` | list<string> | no | One of: `caption_only`, `compilation`, `moments`, `trailer`, `voiceover`. |
| `generationConfig.numGenerations` | number | no |  |
| `generationConfig.minDurationSeconds` | number | no |  |
| `generationConfig.maxDurationSeconds` | number | no |  |
| `generationConfig.sourceStartTime` | number | no |  |
| `generationConfig.sourceEndTime` | number | no |  |
| `renderingConfig.showWatermark` | boolean | no |  |
| `renderingConfig.subtitles` | boolean | no |  |
| `renderingConfig.aspectRatio` | list<string> | no | One of: `16:9`, `1:1`, `4:5`, `9:16`, `9:16-split`. |
| `renderingConfig.resolution` | list<string> | no | One of: `1080`, `240`, `360`, `480`, `720`. |
| `renderingConfig.captionStyle` | object | no |  |
| `renderingConfig.captionStyle.desiredFontSize` | number | no |  |
| `renderingConfig.captionStyle.textTransform` | list<string> | no | One of: `initial`, `lowercase`, `uppercase`. |
| `renderingConfig.captionStyle.textColor` | string | no |  |
| `renderingConfig.captionStyle.highlightColor` | string | no |  |
| `renderingConfig.captionStyle.strokeColor` | string | no |  |
| `renderingConfig.captionStyle.position` | list<string> | no | One of: `bottom`, `middle`, `top`. |
| `renderingConfig.captionStyle.fontFamily` | list<string> | no | One of: `Bangers`, `BebasNeue`, `CaptionFont`, `Lato`, `RobotoCondensed`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reelQuality` | list<string> | no | One of: `fallback`, `full_video`, `lite`, `premium`. |
| `generationConfig` | object | no |  |
| `renderingConfig` | object | no |  |
| `stream` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Reka Vision API, this operation is `POST /v1/clips` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reel-v1.md) for the provider-specific parameters and requirements.

