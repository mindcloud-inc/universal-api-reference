# Scrape Creators: Get YouTube Transcript

Retrieves a YouTube video transcript from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-you-tube-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-you-tube-transcript?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-you-tube-transcript?${params}`, {
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
| `url` | string | yes | YouTube video URL |
| `language` | string | no | Transcript language |

## Response

```json
{
  "success": true,
  "data": [
    {
      "captionTracks": [
        {}
      ],
      "credits_remaining": 1,
      "language": "string",
      "success": true,
      "transcript": [
        {}
      ],
      "transcript_only_text": "string",
      "type": "string",
      "url": "https://example.com",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `captionTracks` | array<object> |  |
| `credits_remaining` | number |  |
| `language` | string |  |
| `success` | boolean |  |
| `transcript` | array<object> |  |
| `transcript_only_text` | string |  |
| `type` | string |  |
| `url` | string |  |
| `videoId` | string |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/youtube/video/transcript` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-you-tube-transcript.md) for the provider-specific parameters and requirements.

