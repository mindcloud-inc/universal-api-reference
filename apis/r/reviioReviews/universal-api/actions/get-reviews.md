# Revi.io Reviews: Get Reviews

Retrieves reviews from Revi.io Reviews.

```
GET https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/get-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revi.io Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/get-reviews?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/get-reviews?${params}`, {
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
| `fromId` | string | no | Return reviews with an id_comment greater than this value. |
| `toId` | string | no | Return reviews with an id_comment lower than this value. |
| `fromDate` | string | no | Return reviews after this date or datetime boundary. |
| `toDate` | string | no | Return reviews before this date or datetime boundary. |
| `equalToRating` | number | no | Return reviews with a rating equal to this value. |
| `greaterThanRating` | number | no | Return reviews with a rating greater than this value. |
| `idProduct` | string | no | Filter reviews for a specific product id. |
| `idStore` | string | no | Marketplace store id or comma-separated store ids. |
| `limit` | number | no | Maximum number of reviews to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Envelope containing the returned reviews array. |
| `success` | boolean | Whether the reviews request succeeded. |

## Native endpoint

Through the native Revi.io Reviews API, this operation is `GET /reviews` (base URL `https://api.revi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reviews.md) for the provider-specific parameters and requirements.

