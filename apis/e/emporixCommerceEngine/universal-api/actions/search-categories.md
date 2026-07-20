# Emporix Commerce Engine: Search Categories

Finds categories in Emporix Commerce Engine by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-categories?${params}`, {
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
      "media": [
        {}
      ],
      "metadata": {},
      "name": "Ava Chen",
      "parentId": "string",
      "position": 1,
      "published": true,
      "supercategoriesIds": [
        "string"
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
| `media` | array<object> |  |
| `metadata` | object |  |
| `name` | string |  |
| `parentId` | string |  |
| `position` | number |  |
| `published` | boolean |  |
| `supercategoriesIds` | array<string> |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `POST /category/{{credentials.tenantId}}/categories/search` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-categories.md) for the provider-specific parameters and requirements.

