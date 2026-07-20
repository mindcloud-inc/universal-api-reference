# Scrape Creators: Get TikTok Video Info

Retrieves TikTok video details from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-tik-tok-video-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-tik-tok-video-info?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-tik-tok-video-info?${params}`, {
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
| `url` | string | yes | TikTok video URL |
| `getTranscript` | boolean | no | Include transcript in the video response when supported |
| `region` | string | no | Proxy region |
| `trim` | boolean | no | Return a trimmed response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aweme_detail": {},
      "credits_remaining": 1,
      "success": true,
      "transcript": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aweme_detail` | object |  |
| `credits_remaining` | number |  |
| `success` | boolean |  |
| `transcript` | string |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v2/tiktok/video` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tik-tok-video-info.md) for the provider-specific parameters and requirements.

