# Creatomate: Distribute Elements Over Time

Creates a render that distributes elements over time.

```
POST https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/distribute-elements-over-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Creatomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/distribute-elements-over-time" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "backgroundAudioUrl": "https://example.com",
  "mediaUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/distribute-elements-over-time', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "backgroundAudioUrl": "https://example.com",
    "mediaUrls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `backgroundAudioUrl` | string | yes | Audio track used as the timeline anchor for the fractional distribution. |
| `mediaUrls[]` | array<string> | yes | Ordered list of image or video URLs to distribute evenly over the timeline. |
| `mediaType` | string | no | Whether the distributed media items are images or videos. Default: `image`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `loopVideos` | boolean | no | Whether distributed video elements should loop to fill their fractional duration. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "outputFormat": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Creatomate render ID. |
| `outputFormat` | string | Output format requested for the render. |
| `status` | string | Current render status returned by Creatomate. |
| `url` | string | Direct URL for the rendered output file. |

## Native endpoint

Through the native Creatomate API, this operation is `POST /v2/renders` (base URL `https://api.creatomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/distribute-elements-over-time.md) for the provider-specific parameters and requirements.

