# Mediastack: Search News Sources

Finds news sources in Mediastack.

```
GET https://connect.mindcloud.co/v1/universal/mediastack/latest/actions/search-news-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mediastack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mediastack/latest/actions/search-news-sources?connectionId=$CONNECTION_ID&limit=25&offset=0&search=abc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "search": "abc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mediastack/latest/actions/search-news-sources?${params}`, {
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
| `search` | string | yes | Required search keyword for matching news sources. Example: `abc`. |
| `countries` | string | no | One or more comma-separated 2-letter country codes. Prefix a country with - to exclude it. Example: `us,gb,-de`. |
| `languages` | string | no | One or more comma-separated 2-letter language codes. Prefix a language with - to exclude it. Example: `en,-de`. |
| `categories` | string | no | One or more comma-separated categories. Prefix a category with - to exclude it. Example: `general,technology`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "code": "string",
      "country": "string",
      "language": "string",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | News category for the source. |
| `code` | string | Mediastack source code returned by the runtime response. |
| `country` | string | Two-letter source country code. |
| `language` | string | Two-letter source language code. |
| `name` | string | Display name of the news source. |
| `url` | string | Source website URL. |

## Native endpoint

Through the native Mediastack API, this operation is `GET /sources` (base URL `https://api.mediastack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-news-sources.md) for the provider-specific parameters and requirements.

