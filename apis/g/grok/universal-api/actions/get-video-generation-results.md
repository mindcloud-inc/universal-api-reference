# Grok: Get Video Generation Results

Retrieves results for a video generation request from Grok.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-video-generation-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-video-generation-results?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-video-generation-results?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | Video generation request identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "model": "string",
      "requestId": "string",
      "status": "string",
      "video": {
        "durationSeconds": 1,
        "respectModeration": true,
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `model` | string | Model that produced the video. |
| `requestId` | string | Video generation request identifier. |
| `status` | string | Current lifecycle status for the video generation request. |
| `video` | object | Rendered video details when the request succeeds. |
| `video.durationSeconds` | number | Video duration in seconds. |
| `video.respectModeration` | boolean | Whether the provider moderation policy was enforced for this result. |
| `video.url` | string | Hosted URL for the generated video. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/videos/:request_id` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-generation-results.md) for the provider-specific parameters and requirements.

