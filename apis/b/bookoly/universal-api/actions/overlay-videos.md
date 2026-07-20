# Bookoly: Overlay Videos

Creates an overlay video in Bookoly.

```
POST https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/overlay-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookoly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/overlay-videos" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video": {},
  "video.name": "Ava Chen",
  "video.url": "https://example.com",
  "video.mute": true,
  "overlayVideo": {},
  "overlayVideo.url": "https://example.com",
  "overlayVideo.mute": true,
  "overlayOption": {},
  "overlayOption.position": "bottom_left"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/overlay-videos', {
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
    "overlayVideo": {},
    "overlayVideo.url": "https://example.com",
    "overlayVideo.mute": true,
    "overlayOption": {},
    "overlayOption.position": "bottom_left"
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
| `overlayVideo` | object | yes |  |
| `overlayVideo.url` | string | yes |  |
| `overlayVideo.mute` | boolean | yes |  |
| `overlayOption` | object | yes |  |
| `overlayOption.position` | list | yes | One of: `bottom_left`, `bottom_right`, `center`, `center_bottom`, `center_left`, `center_right`, `center_top`, `top_left`, `top_right`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bookoly API returns.

## Native endpoint

Through the native Bookoly API, this operation is `POST /overlay-videos` (base URL `https://bookoly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/overlay-videos.md) for the provider-specific parameters and requirements.

