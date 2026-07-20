# Vooplayer: Create Video

Creates a new video in Vooplayer.

```
POST https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/create-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vooplayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/create-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "customS3": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/create-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "customS3": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Video name. |
| `url` | string | no | Video URL. |
| `file` | file | no | File to upload. |
| `customS3` | number | yes | 0 or ID of custom integration. |
| `hls` | number | no | 1 to encode or 0 to leave as unsecured. |
| `videoGroup` | number | no | Project ID. |
| `playerSettings` | object | no | Video ID for copying player settings, decoded base64. |
| `create` | number | no | 1 to confirm or 0 to debug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Created video ID. |

## Native endpoint

Through the native Vooplayer API, this operation is `POST /api/createVideo` (base URL `https://api.spotlightr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video.md) for the provider-specific parameters and requirements.

