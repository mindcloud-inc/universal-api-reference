# Tolstoy: Create Video by URL

Creates a new video in Tolstoy from a URL.

```
POST https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/create-video-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tolstoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/create-video-by-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video.videoUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/create-video-by-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "video.videoUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `video.videoUrl` | string | yes | Hosted video URL |
| `video.name` | string | no | Optional video name |
| `video.posterUrl` | string | no | Optional poster image URL |
| `video.gifUrl` | string | no | Optional animated GIF URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created Tolstoy video id |

## Native endpoint

Through the native Tolstoy API, this operation is `POST /videos/video` (base URL `https://api.gotolstoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video-by-url.md) for the provider-specific parameters and requirements.

