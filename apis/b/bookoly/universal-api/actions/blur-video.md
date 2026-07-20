# Bookoly: Blur Video

Blurs a selected area of a video in Bookoly.

```
POST https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/blur-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookoly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/blur-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video": {},
  "video.name": "Ava Chen",
  "video.url": "https://example.com",
  "video.mute": true,
  "blurOption": {},
  "blurOption.point": {},
  "blurOption.point.x": 1,
  "blurOption.point.y": 1,
  "blurOption.box_width": 1,
  "blurOption.box_height": 1,
  "blurOption.power": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/blur-video', {
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
    "blurOption": {},
    "blurOption.point": {},
    "blurOption.point.x": 1,
    "blurOption.point.y": 1,
    "blurOption.box_width": 1,
    "blurOption.box_height": 1,
    "blurOption.power": 1
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
| `blurOption` | object | yes |  |
| `blurOption.point` | object | yes |  |
| `blurOption.point.x` | number | yes |  |
| `blurOption.point.y` | number | yes |  |
| `blurOption.box_width` | number | yes |  |
| `blurOption.box_height` | number | yes |  |
| `blurOption.power` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bookoly API returns.

## Native endpoint

Through the native Bookoly API, this operation is `POST /blur-a-video` (base URL `https://bookoly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/blur-video.md) for the provider-specific parameters and requirements.

