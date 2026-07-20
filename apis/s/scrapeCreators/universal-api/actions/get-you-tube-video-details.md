# Scrape Creators: Get YouTube Video Details

Retrieves YouTube video or Short details from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-you-tube-video-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-you-tube-video-details?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-you-tube-video-details?${params}`, {
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
| `url` | string | yes | YouTube video or short URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "captionTracks": [
        {}
      ],
      "channel": {},
      "credits_remaining": 1,
      "description": "string",
      "durationFormatted": "string",
      "durationMs": 1,
      "genre": "string",
      "id": "string",
      "keywords": [
        "string"
      ],
      "publishDate": "string",
      "success": true,
      "thumbnail": "string",
      "title": "string",
      "type": "string",
      "watchNextVideos": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `captionTracks` | array<object> |  |
| `channel` | object |  |
| `credits_remaining` | number |  |
| `description` | string |  |
| `durationFormatted` | string |  |
| `durationMs` | number |  |
| `genre` | string |  |
| `id` | string |  |
| `keywords` | array<string> |  |
| `publishDate` | string |  |
| `success` | boolean |  |
| `thumbnail` | string |  |
| `title` | string |  |
| `type` | string |  |
| `watchNextVideos` | array<object> |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/youtube/video` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-you-tube-video-details.md) for the provider-specific parameters and requirements.

