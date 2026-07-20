# Bookoly: Crop Video

Crops a video to a selected area in Bookoly.

```
POST https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/crop-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookoly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/crop-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video": {},
  "video.name": "Ava Chen",
  "video.url": "https://example.com",
  "video.mute": true,
  "cropOption": {},
  "cropOption.point": {},
  "cropOption.point.x": 1,
  "cropOption.point.y": 1,
  "cropOption.width": 1,
  "cropOption.height": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/crop-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "video": {},
    "video.name": "Ava Chen",
    "video.url": "https://example.com",
    "video.mute": true,
    "cropOption": {},
    "cropOption.point": {},
    "cropOption.point.x": 1,
    "cropOption.point.y": 1,
    "cropOption.width": 1,
    "cropOption.height": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `video` | object | yes |  |
| `video.name` | string | yes |  |
| `video.url` | string | yes |  |
| `video.mute` | boolean | yes |  |
| `cropOption` | object | yes |  |
| `cropOption.point` | object | yes |  |
| `cropOption.point.x` | number | yes |  |
| `cropOption.point.y` | number | yes |  |
| `cropOption.width` | number | yes |  |
| `cropOption.height` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bookoly API returns.

## Native endpoint

Through the native Bookoly API, this operation is `POST /crop-a-video` (base URL `https://bookoly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crop-video.md) for the provider-specific parameters and requirements.

