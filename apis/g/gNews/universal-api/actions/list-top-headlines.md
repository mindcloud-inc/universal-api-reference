# GNews: List Top Headlines

Retrieves current top news headlines from GNews.

```
GET https://connect.mindcloud.co/v1/universal/gNews/latest/actions/list-top-headlines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GNews `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gNews/latest/actions/list-top-headlines?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gNews/latest/actions/list-top-headlines?${params}`, {
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
| `q` | string | no | Keywords used to find relevant headlines. |
| `category` | string | no | Filter headlines by category. |
| `lang` | string | no | Filter headlines by article language code. |
| `country` | string | no | Filter headlines by country code. |
| `max` | number | no | Maximum number of articles to return. |
| `page` | number | no | Page number to return. |
| `from` | date | no | Only include articles published on or after this date and time. |
| `to` | date | no | Only include articles published on or before this date and time. |
| `nullable` | string | no | Fields allowed to return null values. |
| `truncate` | string | no | Truncate the content field when set to content. |

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
| `source.id` | string |  |
| `source.name` | string |  |
| `source.url` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native GNews API, this operation is `GET /top-headlines` (base URL `https://gnews.io/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-top-headlines.md) for the provider-specific parameters and requirements.

