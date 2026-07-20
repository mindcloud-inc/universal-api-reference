# gotoHuman: Update Review Request

Updates an existing review request in gotoHuman.

```
PUT https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/update-review-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gotoHuman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/update-review-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "updateForReviewId": "string",
  "formId": "string",
  "fields": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/update-review-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "updateForReviewId": "string",
    "formId": "string",
    "fields": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateForReviewId` | string | yes | The review ID to update. |
| `formId` | string | yes | The ID of the review template / form. |
| `fields` | string | yes | JSON object of updated field values for the review request. |
| `assignToGroups` | string | no | JSON array string of reviewer group IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extReviewerLinks": [
        {}
      ],
      "gthLink": "https://example.com",
      "reviewId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extReviewerLinks` | array<object> | External reviewer links when external reviewers were added. |
| `gthLink` | string | Link to the review in gotoHuman. |
| `reviewId` | string | The updated review request ID. |

## Native endpoint

Through the native gotoHuman API, this operation is `POST /requestReview` (base URL `https://api.gotohuman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-review-request.md) for the provider-specific parameters and requirements.

