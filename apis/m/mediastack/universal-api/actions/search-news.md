# Mediastack: Search News

Finds news articles in Mediastack.

```
GET https://connect.mindcloud.co/v1/universal/mediastack/latest/actions/search-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mediastack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mediastack/latest/actions/search-news?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mediastack/latest/actions/search-news?${params}`, {
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
| `keywords` | string | no | One or more comma-separated search keywords. Prefix a keyword with - to exclude it. Example: `tennis, economy, -rumor`. |
| `categories` | string | no | One or more comma-separated categories. Prefix a category with - to exclude it. Example: `business,-sports`. |
| `countries` | string | no | One or more comma-separated 2-letter country codes. Prefix a country with - to exclude it. Example: `us,gb,-de`. |
| `languages` | string | no | One or more comma-separated 2-letter language codes. Prefix a language with - to exclude it. Example: `en,-de`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sources` | string | no | One or more comma-separated source codes, such as abc-news. Prefix a source code with - to exclude it. Example: `cnn,-bbc`. |
| `date` | string | no | Optional date or date range, such as 2026-04-30 or 2026-04-01,2026-04-30. Example: `2026-04-30 or 2026-04-01,2026-04-30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "category": "string",
      "country": "string",
      "description": "string",
      "image": "https://example.com",
      "language": "string",
      "published_at": "2026-05-07T12:00:00.000Z",
      "source": "Ava Chen",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `category` | string |  |
| `country` | string |  |
| `description` | string |  |
| `image` | string |  |
| `language` | string |  |
| `published_at` | date |  |
| `source` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Mediastack API, this operation is `GET /news` (base URL `https://api.mediastack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-news.md) for the provider-specific parameters and requirements.

