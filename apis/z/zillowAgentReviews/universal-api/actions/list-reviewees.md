# Zillow Agent Reviews: List reviewees

Retrieves reviewees from Zillow Agent Reviews.

```
GET https://connect.mindcloud.co/v1/universal/zillowAgentReviews/latest/actions/list-reviewees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow Agent Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowAgentReviews/latest/actions/list-reviewees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowAgentReviews/latest/actions/list-reviewees?${params}`, {
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
      "AccountIdReviewee": "string",
      "AverageReviewRating": 1,
      "BridgeModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "ReviewCount": 1,
      "RevieweeBusinessName": "Ava Chen",
      "RevieweeEmail": "ava@example.com",
      "RevieweeFullName": "Ava Chen",
      "RevieweeKey": "string",
      "RevieweeProfileURL": "https://example.com",
      "RevieweeScreenName": "Ava Chen",
      "RevieweeTitle": "string",
      "ReviewRequestURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountIdReviewee` | string | Primary identifier for reviewees. |
| `AverageReviewRating` | number | Reviewee's average rating. |
| `BridgeModificationTimestamp` | date | Timestamp for the latest Bridge-side modification. |
| `ReviewCount` | number | Number of reviews for the reviewee. |
| `RevieweeBusinessName` | string | Reviewee business name. |
| `RevieweeEmail` | string | Reviewee email. |
| `RevieweeFullName` | string | Reviewee full name. |
| `RevieweeKey` | string | Bridge primary key for reviewees. |
| `RevieweeProfileURL` | string | Reviewee profile URL. |
| `RevieweeScreenName` | string | Reviewee screen name. |
| `RevieweeTitle` | string | Reviewee title. |
| `ReviewRequestURL` | string | Review request URL. |

## Native endpoint

Through the native Zillow Agent Reviews API, this operation is `GET /OData/reviews/Reviewees` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reviewees.md) for the provider-specific parameters and requirements.

