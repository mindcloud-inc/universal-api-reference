# World News API: Extract News

Extracts a news article from a URL using World News API.

```
GET https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/extract-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/extract-news?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fwww.beijingnews.net%2Fnews%2F278983641%2Fchina-beijing-wang-huning-new-zealand-house-of-representatives-speaker-meeting-cn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://www.beijingnews.net/news/278983641/china-beijing-wang-huning-new-zealand-house-of-representatives-speaker-meeting-cn"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/extract-news?${params}`, {
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
| `analyze` | boolean | no | When true, perform full article analysis during extraction. |
| `url` | string | yes | Article URL to extract structured news data from. Default: `https://www.beijingnews.net/news/278983641/china-beijing-wang-huning-new-zealand-house-of-representatives-speaker-meeting-cn`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "authors": [
        "string"
      ],
      "image": "string",
      "images": [
        {}
      ],
      "language": "string",
      "publish_date": "string",
      "text": "string",
      "title": "string",
      "url": "https://example.com",
      "video": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string | Primary article author. |
| `authors` | array<string> | Article authors. |
| `image` | string | Primary image URL for the article. |
| `images` | array<object> | Images discovered on the article page. |
| `language` | string | Detected article language. |
| `publish_date` | string | Article publish date/time. |
| `text` | string | Extracted article body text. |
| `title` | string | Extracted article title. |
| `url` | string | Canonical article URL. |
| `video` | string | Primary video URL when available. |

## Native endpoint

Through the native World News API API, this operation is `GET /extract-news` (base URL `https://api.worldnewsapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-news.md) for the provider-specific parameters and requirements.

