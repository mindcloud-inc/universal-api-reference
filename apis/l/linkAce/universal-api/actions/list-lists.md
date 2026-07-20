# LinkAce: List Lists

Retrieves saved bookmark lists from LinkAce.

```
GET https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/list-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkAce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/list-lists?${params}`, {
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
      "current_page": 1,
      "data": [
        {}
      ],
      "first_page_url": "https://example.com",
      "from": 1,
      "last_page": 1,
      "last_page_url": "https://example.com",
      "next_page_url": "https://example.com",
      "path": "string",
      "per_page": "string",
      "prev_page_url": "https://example.com",
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number | Current page number. |
| `data` | array<object> | Resources returned for this page. |
| `first_page_url` | string | First page URL. |
| `from` | number | Index of the first result on this page. |
| `last_page` | number | Last available page number. |
| `last_page_url` | string | Last page URL. |
| `next_page_url` | string | Next page URL when available. |
| `path` | string | Base API path for this paginator. |
| `per_page` | string | Page size returned by the API. |
| `prev_page_url` | string | Previous page URL when available. |
| `to` | number | Index of the last result on this page. |
| `total` | number | Total results in the current paginator. |

## Native endpoint

Through the native LinkAce API, this operation is `GET /lists` (base URL `https://demo.linkace.org/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lists.md) for the provider-specific parameters and requirements.

