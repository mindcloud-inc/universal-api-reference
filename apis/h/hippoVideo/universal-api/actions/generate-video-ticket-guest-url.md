# Hippo Video: Generate Video Ticket Guest URL

Retrieves a guest URL for Hippo Video ticket recording.

```
GET https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/generate-video-ticket-guest-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hippo Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/generate-video-ticket-guest-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/generate-video-ticket-guest-url?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `url` | string |  |

## Native endpoint

Through the native Hippo Video API, this operation is `GET /api/v1/me/video/guest_url/` (base URL `https://www.hippovideo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-video-ticket-guest-url.md) for the provider-specific parameters and requirements.

