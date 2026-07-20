# ScrapeGraphAI: Submit Feedback

Submits rating feedback for a ScrapeGraphAI request.

```
POST https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/submit-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeGraphAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/submit-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rating": "5",
  "requestId": "f1248013-7f30-46db-ab8a-484038415082"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/submit-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rating": "5",
    "requestId": "f1248013-7f30-46db-ab8a-484038415082"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedbackText` | string | no | Optional free-form feedback text. Example: `Great markdown conversion quality.`. |
| `rating` | number | yes | Rating value from 0 to 5. Example: `5`. |
| `requestId` | string | yes | Request ID the feedback refers to. Example: `f1248013-7f30-46db-ab8a-484038415082`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapeGraphAI API returns.

## Native endpoint

Through the native ScrapeGraphAI API, this operation is `POST /feedback` (base URL `https://api.scrapegraphai.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-feedback.md) for the provider-specific parameters and requirements.

