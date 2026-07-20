# Monica CRM: List Tags

Retrieves tags from Monica CRM.

```
GET https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monica CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/list-tags?${params}`, {
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
        {}
      ],
      "links": {
        "first": "https://example.com",
        "last": "https://example.com",
        "next": "https://example.com",
        "prev": "https://example.com"
      },
      "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "path": "string",
        "per_page": 1,
        "to": 1,
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
| `data` | array<object> |  |
| `links.first` | string |  |
| `links.last` | string |  |
| `links.next` | string |  |
| `links.prev` | string |  |
| `meta.current_page` | number |  |
| `meta.from` | number |  |
| `meta.last_page` | number |  |
| `meta.path` | string |  |
| `meta.per_page` | number |  |
| `meta.to` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native Monica CRM API, this operation is `GET /tags` (base URL `https://app.monicahq.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

