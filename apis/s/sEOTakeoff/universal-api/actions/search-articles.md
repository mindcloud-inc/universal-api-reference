# SEOTakeoff: Search Articles



```
GET https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/search-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEOTakeoff `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/search-articles?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/search-articles?${params}`, {
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
| `query` | string | yes | Article title or keyword search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "error_message": "string",
      "id": "string",
      "keyword": "string",
      "published_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "website_id": "string",
      "website_name": "Ava Chen",
      "word_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `error_message` | string |  |
| `id` | string |  |
| `keyword` | string |  |
| `published_at` | date |  |
| `status` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `website_id` | string |  |
| `website_name` | string |  |
| `word_count` | number |  |

## Native endpoint

Through the native SEOTakeoff API, this operation is `GET /api/zapier/articles/search` (base URL `https://api.seotakeoff.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-articles.md) for the provider-specific parameters and requirements.

