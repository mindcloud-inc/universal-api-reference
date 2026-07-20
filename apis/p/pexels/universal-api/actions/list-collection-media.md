# Pexels: List Collection Media

Retrieves media from a Pexels collection.

```
GET https://connect.mindcloud.co/v1/universal/pexels/latest/actions/list-collection-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pexels `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pexels/latest/actions/list-collection-media?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pexels/latest/actions/list-collection-media?${params}`, {
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
| `id` | string | yes | Pexels collection ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no | Optional media filter: photos or videos. |
| `sort` | string | no | Order of media in the collection: asc or desc. Defaults to asc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "media": [
        {}
      ],
      "next_page": "string",
      "page": 1,
      "per_page": 1,
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
| `id` | string | Pexels collection ID. |
| `media` | array<object> | Photo and video objects in the collection. Each item includes a type field. |
| `next_page` | string | Next page URL when available. |
| `page` | number | Current page number. |
| `per_page` | number | Number of results returned per page. |
| `prev_page` | string | Previous page URL when available. |
| `total_results` | number | Total number of matching results. |

## Native endpoint

Through the native Pexels API, this operation is `GET /v1/collections/:id` (base URL `https://api.pexels.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-collection-media.md) for the provider-specific parameters and requirements.

