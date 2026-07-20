# Shopper Approved: Get Review Aggregate Statistics

Retrieves review aggregate statistics from Shopper Approved.

```
GET https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-review-aggregate-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopper Approved `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-review-aggregate-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-review-aggregate-statistics?${params}`, {
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
      "1Star": 1,
      "2Star": 1,
      "3Star": 1,
      "4Star": 1,
      "5Star": 1,
      "averageRating": 1,
      "otherQuestions": {},
      "siteId": "string",
      "siteLabel": "string",
      "siteUrl": "https://example.com",
      "totalReviews": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `1Star` | number |  |
| `2Star` | number |  |
| `3Star` | number |  |
| `4Star` | number |  |
| `5Star` | number |  |
| `averageRating` | number |  |
| `otherQuestions` | object |  |
| `siteId` | string |  |
| `siteLabel` | string |  |
| `siteUrl` | string |  |
| `totalReviews` | number |  |

## Native endpoint

Through the native Shopper Approved API, this operation is `GET /aggregates/reviews/:siteid` (base URL `https://api.shopperapproved.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-review-aggregate-statistics.md) for the provider-specific parameters and requirements.

