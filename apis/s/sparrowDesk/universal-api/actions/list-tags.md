# SparrowDesk: List Tags

Retrieves tags from SparrowDesk.

```
GET https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-tags?${params}`, {
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
      "createdAt": 1,
      "id": 1,
      "name": "Ava Chen",
      "pages": {
        "nextCursor": "string",
        "nextUrl": "https://example.com",
        "perPage": 1
      },
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Creation timestamp. |
| `id` | number | Tag ID. |
| `name` | string | Tag name. |
| `pages.nextCursor` | string | Cursor for the next page. |
| `pages.nextUrl` | string | Next page URL. |
| `pages.perPage` | number | Page size. |
| `totalCount` | number | Total number of tags. |

## Native endpoint

Through the native SparrowDesk API, this operation is `GET /tags` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

