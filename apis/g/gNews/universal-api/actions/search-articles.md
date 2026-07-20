# GNews: Search Articles

Searches GNews for news articles by keyword.

```
GET https://connect.mindcloud.co/v1/universal/gNews/latest/actions/search-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GNews `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gNews/latest/actions/search-articles?connectionId=$CONNECTION_ID&limit=25&offset=0&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gNews/latest/actions/search-articles?${params}`, {
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
| `q` | string | yes | Keywords used to find matching news articles. |
| `lang` | string | no | Filter returned articles by language code. |
| `country` | string | no | Filter returned articles by publication country code. |
| `max` | number | no | Maximum number of articles to return per page. |
| `searchIn` | string | no | Choose which article fields are searched for the query terms. |
| `nullable` | string | no | Allow selected attributes to be returned as null. |
| `from` | date | no | Only include articles published on or after this ISO 8601 timestamp. |
| `to` | date | no | Only include articles published on or before this ISO 8601 timestamp. |
| `sortBy` | string | no | Sort articles by publication date or relevance. |
| `page` | number | no | Page number to return. |
| `truncate` | string | no | Truncate selected fields such as content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "description": "string",
      "id": "string",
      "image": "string",
      "lang": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "source": {
        "country": "string",
        "id": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
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
| `content` | string |  |
| `description` | string |  |
| `id` | string |  |
| `image` | string |  |
| `lang` | string |  |
| `publishedAt` | date |  |
| `source.country` | string |  |
| `source.id` | string |  |
| `source.name` | string |  |
| `source.url` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native GNews API, this operation is `GET /search` (base URL `https://gnews.io/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-articles.md) for the provider-specific parameters and requirements.

