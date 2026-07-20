# Saastic: List Reviews

Retrieves reviews from Saastic.

```
GET https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saastic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-reviews?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-reviews?${params}`, {
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
      "created_at": 1,
      "has_reply": true,
      "id": 1,
      "rating": {
        "image_link": "https://example.com",
        "label": "string",
        "score": 1
      },
      "review": "string",
      "review_html": "string",
      "reviewer": {
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
| `rating.image_link` | string |  |
| `rating.label` | string |  |
| `rating.score` | number |  |
| `review` | string |  |
| `review_html` | string |  |
| `reviewer.first_name` | string |  |
| `reviewer.last_name` | string |  |
| `reviewer.name` | string |  |
| `score` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Saastic API, this operation is `GET /beacon/reviews` (base URL `https://api.moregoodreviews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reviews.md) for the provider-specific parameters and requirements.

