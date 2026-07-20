# Reka Vision: Trigger Objects (V2)

Creates an object detection and tracking job in Reka Vision.

```
POST https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/trigger-objects-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/trigger-objects-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/trigger-objects-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoId` | string | yes |  |
| `force` | boolean | no |  |
| `personLocalization.maxFps` | number | no |  |
| `personLocalization.maxFailedFrames` | number | no |  |
| `personLocalization.numPhotosPerPerson` | number | no |  |
| `personLocalization.maxObjectsPerChunk` | number | no |  |
| `personLocalization.conf` | number | no |  |
| `personLocalization.iou` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personLocalization` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feature": "string",
      "status": "string",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feature` | string |  |
| `status` | string |  |
| `videoId` | string |  |

## Native endpoint

Through the native Reka Vision API, this operation is `POST /v2/videos/:videoId/features/objects` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-objects-v2.md) for the provider-specific parameters and requirements.

