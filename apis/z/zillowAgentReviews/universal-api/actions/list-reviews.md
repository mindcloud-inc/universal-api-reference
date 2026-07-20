# Zillow Agent Reviews: List reviews

Retrieves agent reviews from Zillow Agent Reviews.

```
GET https://connect.mindcloud.co/v1/universal/zillowAgentReviews/latest/actions/list-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow Agent Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowAgentReviews/latest/actions/list-reviews?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowAgentReviews/latest/actions/list-reviews?${params}`, {
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
      "AccountIdReviewer": "string",
      "BridgeModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "Description": "string",
      "FreeFormLocation": "string",
      "PropertyId": "string",
      "PropertyLocationNames": "Ava Chen",
      "Rating": 1,
      "RegionId": "string",
      "RegionLocationNames": "Ava Chen",
      "ReviewDate": "2026-05-07T12:00:00.000Z",
      "RevieweeKey": "string",
      "ReviewerFullName": "Ava Chen",
      "ReviewerScreenName": "Ava Chen",
      "ReviewId": "string",
      "ReviewKey": "string",
      "ServiceProviderDesc": "string",
      "ServiceYear": 1,
      "TeamLeadAccountId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountIdReviewee` | string | Primary identifier for the reviewee. |
| `AccountIdReviewer` | string | Primary identifier for the reviewer. |
| `BridgeModificationTimestamp` | date | Timestamp for the latest Bridge-side modification. |
| `Description` | string | Review content. |
| `FreeFormLocation` | string | Free-form location text. |
| `PropertyId` | string | Property identifier. |
| `PropertyLocationNames` | string | Property location names. |
| `Rating` | number | Review rating. |
| `RegionId` | string | Region identifier. |
| `RegionLocationNames` | string | Region location names. |
| `ReviewDate` | date | Review date. |
| `RevieweeKey` | string | Bridge foreign key for reviewees. |
| `ReviewerFullName` | string | Reviewer's full name. |
| `ReviewerScreenName` | string | Reviewer's screen name. |
| `ReviewId` | string | Primary identifier for reviews. |
| `ReviewKey` | string | Bridge primary key for reviews. |
| `ServiceProviderDesc` | string | Service provider description. |
| `ServiceYear` | number | Service year. |
| `TeamLeadAccountId` | string | Primary identifier for the team lead. |

## Native endpoint

Through the native Zillow Agent Reviews API, this operation is `GET /OData/reviews/Reviews` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reviews.md) for the provider-specific parameters and requirements.

