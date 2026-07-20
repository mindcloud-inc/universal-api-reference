# Polymer: Update Job Application Review

Updates an existing job application review in Polymer.

```
PUT https://connect.mindcloud.co/v1/universal/polymer/latest/actions/update-job-application-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polymer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/polymer/latest/actions/update-job-application-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/polymer/latest/actions/update-job-application-review', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | Updated review HTML body. |
| `job_application_id` | string | no | Numeric Polymer job application ID. |
| `rating` | string | no | Updated review rating: strong_yes, weak_yes, weak_no, strong_no, or no_rating. |
| `review_id` | string | no | Numeric Polymer review ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Polymer API returns.

## Native endpoint

Through the native Polymer API, this operation is `PUT /job_applications/:job_application_id/reviews/:review_id` (base URL `https://api.polymer.co/v1/hire`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job-application-review.md) for the provider-specific parameters and requirements.

