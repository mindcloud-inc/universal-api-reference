# Scrape Creators: Get TikTok Transcript

Retrieves a TikTok video transcript from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-tik-tok-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-tik-tok-transcript?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-tik-tok-transcript?${params}`, {
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
| `language` | string | no | Transcript language |
| `useAiAsFallback` | boolean | no | Use AI if a transcript is not directly available |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_remaining": 1,
      "id": "string",
      "success": true,
      "transcript": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number |  |
| `id` | string |  |
| `success` | boolean |  |
| `transcript` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/tiktok/video/transcript` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tik-tok-transcript.md) for the provider-specific parameters and requirements.

