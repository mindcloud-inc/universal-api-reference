# ScrapingDog: Search YouTube

Retrieves YouTube search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-you-tube
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-you-tube?connectionId=$CONNECTION_ID&searchQuery=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchQuery": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-you-tube?${params}`, {
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
| `searchQuery` | string | yes | Search query for YouTube. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels_new_to_you": {
        "channel": {
          "link": "https://example.com",
          "name": "Ava Chen",
          "thumbmail": "string",
          "verified": true
        },
        "description": "string",
        "length": "string",
        "link": "https://example.com",
        "position": 1,
        "published_date": "string",
        "thumbnail": {
          "rich": "string",
          "static": "string"
        },
        "title": "string",
        "views": "string"
      },
      "from_related_searches": {
        "channel": {
          "link": "https://example.com",
          "name": "Ava Chen",
          "thumbmail": "string",
          "verified": true
        },
        "description": "string",
        "length": "string",
        "link": "https://example.com",
        "position": 1,
        "published_date": "string",
        "thumbnail": {
          "rich": "string",
          "static": "string"
        },
        "title": "string",
        "views": "string"
      },
      "pagination": {
        "current": "string",
        "next": "string",
        "next_page_token": "string"
      },
      "popular_today": {
        "channel": {
          "link": "https://example.com",
          "name": "Ava Chen",
          "thumbmail": "string",
          "verified": true
        },
        "description": "string",
        "extensions": [
          "string"
        ],
        "length": "string",
        "link": "https://example.com",
        "position": 1,
        "published_date": "string",
        "thumbnail": {
          "rich": "string",
          "static": "string"
        },
        "title": "string",
        "views": "string"
      },
      "video_results": {
        "channel": {
          "link": "https://example.com",
          "name": "Ava Chen",
          "thumbmail": "string",
          "verified": true
        },
        "description": "string",
        "length": "string",
        "link": "https://example.com",
        "position": 1,
        "published_date": "string",
        "thumbnail": {
          "rich": "string",
          "static": "string"
        },
        "title": "string",
        "views": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels_new_to_you` | array<object> |  |
| `channels_new_to_you.channel` | object |  |
| `channels_new_to_you.channel.link` | string |  |
| `channels_new_to_you.channel.name` | string |  |
| `channels_new_to_you.channel.thumbmail` | string |  |
| `channels_new_to_you.channel.verified` | boolean |  |
| `channels_new_to_you.description` | string |  |
| `channels_new_to_you.length` | string |  |
| `channels_new_to_you.link` | string |  |
| `channels_new_to_you.position` | number |  |
| `channels_new_to_you.published_date` | string |  |
| `channels_new_to_you.thumbnail` | object |  |
| `channels_new_to_you.thumbnail.rich` | string |  |
| `channels_new_to_you.thumbnail.static` | string |  |
| `channels_new_to_you.title` | string |  |
| `channels_new_to_you.views` | string |  |
| `from_related_searches` | array<object> |  |
| `from_related_searches.channel` | object |  |
| `from_related_searches.channel.link` | string |  |
| `from_related_searches.channel.name` | string |  |
| `from_related_searches.channel.thumbmail` | string |  |
| `from_related_searches.channel.verified` | boolean |  |
| `from_related_searches.description` | string |  |
| `from_related_searches.length` | string |  |
| `from_related_searches.link` | string |  |
| `from_related_searches.position` | number |  |
| `from_related_searches.published_date` | string |  |
| `from_related_searches.thumbnail` | object |  |
| `from_related_searches.thumbnail.rich` | string |  |
| `from_related_searches.thumbnail.static` | string |  |
| `from_related_searches.title` | string |  |
| `from_related_searches.views` | string |  |
| `pagination` | object |  |
| `pagination.current` | string |  |
| `pagination.next` | string |  |
| `pagination.next_page_token` | string |  |
| `popular_today` | array<object> |  |
| `popular_today.channel` | object |  |
| `popular_today.channel.link` | string |  |
| `popular_today.channel.name` | string |  |
| `popular_today.channel.thumbmail` | string |  |
| `popular_today.channel.verified` | boolean |  |
| `popular_today.description` | string |  |
| `popular_today.extensions` | array<string> |  |
| `popular_today.length` | string |  |
| `popular_today.link` | string |  |
| `popular_today.position` | number |  |
| `popular_today.published_date` | string |  |
| `popular_today.thumbnail` | object |  |
| `popular_today.thumbnail.rich` | string |  |
| `popular_today.thumbnail.static` | string |  |
| `popular_today.title` | string |  |
| `popular_today.views` | string |  |
| `video_results` | array<object> |  |
| `video_results.channel` | object |  |
| `video_results.channel.link` | string |  |
| `video_results.channel.name` | string |  |
| `video_results.channel.thumbmail` | string |  |
| `video_results.channel.verified` | boolean |  |
| `video_results.description` | string |  |
| `video_results.length` | string |  |
| `video_results.link` | string |  |
| `video_results.position` | number |  |
| `video_results.published_date` | string |  |
| `video_results.thumbnail` | object |  |
| `video_results.thumbnail.rich` | string |  |
| `video_results.thumbnail.static` | string |  |
| `video_results.title` | string |  |
| `video_results.views` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /youtube/search` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-you-tube.md) for the provider-specific parameters and requirements.

