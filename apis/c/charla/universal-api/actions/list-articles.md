# Charla: List Articles

Retrieves articles from Charla.

```
GET https://connect.mindcloud.co/v1/universal/charla/latest/actions/list-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Charla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/charla/latest/actions/list-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/charla/latest/actions/list-articles?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": 1,
          "slug": "string",
          "status": "string",
          "title": "string",
          "trained_at": "2026-05-07T12:00:00.000Z",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "visibility": "string"
        }
      ],
      "paging": {
        "has_next": true,
        "next_cursor": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_at` | date |  |
| `data[].description` | string |  |
| `data[].id` | number |  |
| `data[].slug` | string |  |
| `data[].status` | string |  |
| `data[].title` | string |  |
| `data[].trained_at` | date |  |
| `data[].updated_at` | date |  |
| `data[].visibility` | string |  |
| `paging.has_next` | boolean |  |
| `paging.next_cursor` | number |  |
| `paging.total` | number |  |

## Native endpoint

Through the native Charla API, this operation is `GET /kb/articles` (base URL `https://api.charla.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-articles.md) for the provider-specific parameters and requirements.

