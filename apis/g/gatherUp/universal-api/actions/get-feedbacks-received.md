# GatherUp: Get Feedbacks Received

Retrieves received customer feedback from GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/get-feedbacks-received
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/get-feedbacks-received?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/get-feedbacks-received?${params}`, {
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
| `businessId` | number | no | Business id (or multiple comma-separated ids.) |
| `from` | string | no | Received from |
| `to` | string | no | Received to |
| `page` | number | no | Page Default: `1`. |
| `minRecommend` | number | no | Minimal recommend |
| `maxRecommend` | number | no | Maximal recommend |
| `showSurvey` | number | no | Include Survey Question results |
| `customerId` | number | no | Return feedbacks only for a specific customer |
| `visible` | number | no | Return feedbacks visible or not |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorEmail": "ava@example.com",
      "authorName": "Ava Chen",
      "body": "string",
      "businessId": "string",
      "count": 1,
      "customId": "string",
      "dateOfReview": "string",
      "errorCode": 1,
      "errorMessage": "string",
      "feedbackId": "string",
      "jobId": "string",
      "negativeDetails": "string",
      "page": 1,
      "pages": 1,
      "perPage": 1,
      "rating": 1,
      "recommend": 1,
      "showReview": "string",
      "tags": "string",
      "userResponse": "string",
      "userResponseTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorEmail` | string |  |
| `authorName` | string |  |
| `body` | string |  |
| `businessId` | string |  |
| `count` | number |  |
| `customId` | string |  |
| `dateOfReview` | string |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `feedbackId` | string |  |
| `jobId` | string |  |
| `negativeDetails` | string |  |
| `page` | number |  |
| `pages` | number |  |
| `perPage` | number |  |
| `rating` | number |  |
| `recommend` | number |  |
| `showReview` | string |  |
| `tags` | string |  |
| `userResponse` | string |  |
| `userResponseTime` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /feedbacks/get` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feedbacks-received.md) for the provider-specific parameters and requirements.

