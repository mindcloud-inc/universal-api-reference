# More Good Reviews: List Customer Reviews

Retrieves reviews for a customer in More Good Reviews.

```
GET https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customer-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a More Good Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customer-reviews?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customer-reviews?${params}`, {
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
| `id` | string | yes | The customer identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "has_reply": true,
      "id": 1,
      "is_duplicate": 1,
      "is_hidden": 1,
      "rating": {
        "color": "string",
        "default_image_link": "https://example.com",
        "icon": "string",
        "id": 1,
        "image_link": "https://example.com",
        "label": "string",
        "score": 1,
        "uuid": "string"
      },
      "review": "string",
      "review_html": "string",
      "reviewer": {
        "color": "string",
        "first_name": "Ava",
        "last_name": "Chen",
        "name": "Ava Chen"
      },
      "score": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `has_reply` | boolean |  |
| `id` | number |  |
| `is_duplicate` | number |  |
| `is_hidden` | number |  |
| `rating.color` | string |  |
| `rating.default_image_link` | string |  |
| `rating.icon` | string |  |
| `rating.id` | number |  |
| `rating.image_link` | string |  |
| `rating.label` | string |  |
| `rating.score` | number |  |
| `rating.uuid` | string |  |
| `review` | string |  |
| `review_html` | string |  |
| `reviewer.color` | string |  |
| `reviewer.first_name` | string |  |
| `reviewer.last_name` | string |  |
| `reviewer.name` | string |  |
| `score` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native More Good Reviews API, this operation is `GET /beacon/customers/:id/reviews` (base URL `https://api.moregoodreviews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-reviews.md) for the provider-specific parameters and requirements.

