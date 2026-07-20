# Beds24: List Airbnb Reviews

Retrieves Airbnb guest reviews from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-airbnb-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-airbnb-reviews?connectionId=$CONNECTION_ID&roomId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-airbnb-reviews?${params}`, {
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
| `roomId` | number | yes | Beds24 room ID whose Airbnb reviews should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "overall_rating": 1,
      "public_review": "string",
      "reviewee_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Airbnb review ID. |
| `overall_rating` | number | Overall Airbnb review rating. |
| `public_review` | string | Public review text. |
| `reviewee_id` | string | Airbnb reviewee identifier. |

## Native endpoint

Through the native Beds24 API, this operation is `GET /channels/airbnb/reviews` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-airbnb-reviews.md) for the provider-specific parameters and requirements.

