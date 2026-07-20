# Tettra: List Category Items

Retrieves category items from Tettra.

```
GET https://connect.mindcloud.co/v1/universal/tettra/latest/actions/list-category-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tettra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tettra/latest/actions/list-category-items?connectionId=$CONNECTION_ID&categoryId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tettra/latest/actions/list-category-items?${params}`, {
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
| `categoryId` | number | yes | Category ID to read items from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryItems": [
        {
          "can_update": 1,
          "category_id": 1,
          "color": "string",
          "created_at": "string",
          "icon": "string",
          "id": 1,
          "is_pinned": 1,
          "slug": "string",
          "title": "string",
          "type": "string",
          "updated_at": "string",
          "user_id": "string"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryItems[].can_update` | number |  |
| `categoryItems[].category_id` | number |  |
| `categoryItems[].color` | string |  |
| `categoryItems[].created_at` | string |  |
| `categoryItems[].icon` | string |  |
| `categoryItems[].id` | number |  |
| `categoryItems[].is_pinned` | number |  |
| `categoryItems[].slug` | string |  |
| `categoryItems[].title` | string |  |
| `categoryItems[].type` | string |  |
| `categoryItems[].updated_at` | string |  |
| `categoryItems[].user_id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tettra API, this operation is `GET /teams/85329/categories/:category_id` (base URL `https://app.tettra.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-category-items.md) for the provider-specific parameters and requirements.

