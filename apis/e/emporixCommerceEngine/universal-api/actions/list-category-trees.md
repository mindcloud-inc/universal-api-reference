# Emporix Commerce Engine: List Category Trees

Retrieves category trees from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-category-trees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-category-trees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-category-trees?${params}`, {
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
      "code": "string",
      "description": "string",
      "id": "string",
      "localizedDescription": {},
      "localizedName": {},
      "name": "Ava Chen",
      "position": 1,
      "published": true,
      "subcategories": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `description` | string |  |
| `id` | string |  |
| `localizedDescription` | object |  |
| `localizedName` | object |  |
| `name` | string |  |
| `position` | number |  |
| `published` | boolean |  |
| `subcategories` | array<object> |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /category/{{credentials.tenantId}}/category-trees` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-category-trees.md) for the provider-specific parameters and requirements.

