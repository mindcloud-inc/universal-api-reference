# WiserReview: Get Star Ratings

Retrieves star ratings for a product from WiserReview.

```
GET https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/get-star-ratings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WiserReview `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/get-star-ratings?connectionId=$CONNECTION_ID&listProductId%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listProductId[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiserReview/latest/actions/get-star-ratings?${params}`, {
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
| `listProductId[]` | array<string> | yes | List of product IDs for which to retrieve star ratings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avgrtng": 1,
      "html": "string",
      "isReqSyncWoo": true,
      "pid": "string",
      "prtng": 1,
      "queCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avgrtng` | number | Average rating for the product. |
| `html` | string | Provider-supplied HTML snippet for the rating widget. |
| `isReqSyncWoo` | boolean | Provider flag indicating whether WooCommerce synchronization is required. |
| `pid` | string | Unique product identifier. |
| `prtng` | number | Total number of ratings. |
| `queCount` | number | Count of related questions. |

## Native endpoint

Through the native WiserReview API, this operation is `POST https://rs.wiserreview.com/api/v1/getStarRating` (base URL `https://api.wiserreview.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-star-ratings.md) for the provider-specific parameters and requirements.

