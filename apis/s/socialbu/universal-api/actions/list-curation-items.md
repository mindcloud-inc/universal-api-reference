# Socialbu: List Curation Items

Retrieves curated content items from SocialBu.

```
GET https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/list-curation-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/list-curation-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/list-curation-items?${params}`, {
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
      "author": "string",
      "currentPage": 1,
      "id": 1,
      "items": [
        {}
      ],
      "lastPage": 1,
      "nextPage": 1,
      "title": "string",
      "total": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `currentPage` | number |  |
| `id` | number |  |
| `items` | array<object> |  |
| `lastPage` | number |  |
| `nextPage` | number |  |
| `title` | string |  |
| `total` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Socialbu API, this operation is `GET /curation/items` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-curation-items.md) for the provider-specific parameters and requirements.

