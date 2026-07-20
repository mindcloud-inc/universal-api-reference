# ShopWired: Get a specific category

Retrieves a category from ShopWired by ID.

```
GET https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-category-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShopWired `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-category-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-category-by-id?${params}`, {
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
| `id` | number | yes | The unique identifier of the category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "featured": true,
      "id": 1,
      "image": {
        "url": "https://example.com"
      },
      "slug": "string",
      "sortOrder": 1,
      "title": "string",
      "tradeOnly": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `featured` | boolean |  |
| `id` | number |  |
| `image.url` | string |  |
| `slug` | string |  |
| `sortOrder` | number |  |
| `title` | string |  |
| `tradeOnly` | boolean |  |
| `url` | string |  |

## Native endpoint

Through the native ShopWired API, this operation is `GET /categories/{id}` (base URL `https://api.ecommerceapi.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category-by-id.md) for the provider-specific parameters and requirements.

