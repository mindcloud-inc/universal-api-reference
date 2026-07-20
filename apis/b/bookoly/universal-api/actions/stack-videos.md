# Bookoly: Stack Videos

Creates a stacked video in Bookoly.

```
POST https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/stack-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookoly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/stack-videos" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video": {},
  "video.name": "Ava Chen",
  "video.url": "https://example.com",
  "video.mute": true,
  "secondaryVideo": {},
  "secondaryVideo.url": "https://example.com",
  "secondaryVideo.mute": true,
  "stackOption": {},
  "stackOption.layout": "horizontal"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/stack-videos', {
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
    "secondaryVideo": {},
    "secondaryVideo.url": "https://example.com",
    "secondaryVideo.mute": true,
    "stackOption": {},
    "stackOption.layout": "horizontal"
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
| `secondaryVideo` | object | yes |  |
| `secondaryVideo.url` | string | yes |  |
| `secondaryVideo.mute` | boolean | yes |  |
| `stackOption` | object | yes |  |
| `stackOption.layout` | list | yes | One of: `horizontal`, `vertical`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bookoly API returns.

## Native endpoint

Through the native Bookoly API, this operation is `POST /stack-videos` (base URL `https://bookoly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stack-videos.md) for the provider-specific parameters and requirements.

