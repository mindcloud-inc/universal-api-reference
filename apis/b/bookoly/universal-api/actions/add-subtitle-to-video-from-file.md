# Bookoly: Add Subtitle To Video From File

Adds subtitles from a file to a video in Bookoly.

```
POST https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/add-subtitle-to-video-from-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookoly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/add-subtitle-to-video-from-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video": {},
  "video.name": "Ava Chen",
  "video.url": "https://example.com",
  "subtitle": {},
  "subtitle.type": "ass",
  "subtitle.url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/add-subtitle-to-video-from-file', {
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
    "subtitle": {},
    "subtitle.type": "ass",
    "subtitle.url": "https://example.com"
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
| `subtitle` | object | yes |  |
| `subtitle.type` | list | yes | One of: `ass`. |
| `subtitle.url` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bookoly API returns.

## Native endpoint

Through the native Bookoly API, this operation is `POST /add-subtitle-to-video-from-file` (base URL `https://bookoly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subtitle-to-video-from-file.md) for the provider-specific parameters and requirements.

