# Bookoly: Scale Video

Scales a video to new dimensions in Bookoly.

```
POST https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/scale-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookoly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/scale-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video": {},
  "video.name": "Ava Chen",
  "video.url": "https://example.com",
  "video.mute": true,
  "scaleOption": {},
  "scaleOption.mode": "scale_exact"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/scale-video', {
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
    "scaleOption": {},
    "scaleOption.mode": "scale_exact"
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
| `scaleOption` | object | yes |  |
| `scaleOption.mode` | list | yes | One of: `scale_exact`, `scale_keep_aspect_ratio`, `scale_to_fill`, `scale_to_fit`, `scale_to_height`, `scale_to_width`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bookoly API returns.

## Native endpoint

Through the native Bookoly API, this operation is `POST /scale-a-video` (base URL `https://bookoly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scale-video.md) for the provider-specific parameters and requirements.

