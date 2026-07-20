# Vadootv: Add captions

Creates a captioned video in Vadootv.

```
POST https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/add-captions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadootv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/add-captions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/video.mp4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/add-captions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/video.mp4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the video to caption. Example: `https://example.com/video.mp4`. |
| `language` | string | no | Language of the source video. Example: `English`. |
| `theme` | string | no | Caption theme name. Example: `Hormozi_1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "vid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `vid` | string | Video ID for the captioned output. |

## Native endpoint

Through the native Vadootv API, this operation is `POST /api/add_captions` (base URL `https://aiapi.vadoo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-captions.md) for the provider-specific parameters and requirements.

