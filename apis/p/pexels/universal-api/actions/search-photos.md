# Pexels: Search Photos

Finds photos in Pexels by search query.

```
GET https://connect.mindcloud.co/v1/universal/pexels/latest/actions/search-photos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pexels `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pexels/latest/actions/search-photos?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pexels/latest/actions/search-photos?${params}`, {
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
| `query` | string | yes | Topic to search for, such as Ocean, Tigers, or Group of people working. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orientation` | string | no | Desired photo orientation: landscape, portrait, or square. |
| `size` | string | no | Minimum photo size: large, medium, or small. |
| `color` | string | no | Desired photo color name or hex color code supported by Pexels. |
| `locale` | string | no | Locale for the search, such as en-US, pt-BR, or es-ES. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next_page": "string",
      "page": 1,
      "per_page": 1,
      "photos": [
        {}
      ],
      "prev_page": "string",
      "total_results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `next_page` | string | Next page URL when available. |
| `page` | number | Current page number. |
| `per_page` | number | Number of results returned per page. |
| `photos` | array<object> | Photo results returned by Pexels. |
| `prev_page` | string | Previous page URL when available. |
| `total_results` | number | Total number of matching results. |

## Native endpoint

Through the native Pexels API, this operation is `GET /v1/search` (base URL `https://api.pexels.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-photos.md) for the provider-specific parameters and requirements.

