# MoreApp: Resend Submission

Resends a submission in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/resend-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/resend-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "submissionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/resend-submission', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "submissionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes |  |
| `submissionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "message": "string",
      "scope": "string",
      "status": 1,
      "traceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object | Additional provider error details when present. |
| `message` | string | Provider message describing the resend submission result. |
| `scope` | string | MoreApp error scope for the resend submission response. |
| `status` | number | HTTP-style provider status returned when the submission id is not found. |
| `traceId` | string | MoreApp trace identifier for support and debugging. |

## Native endpoint

Through the native MoreApp API, this operation is `PUT /api/v1.0/customers/{{customerId}}/submissions/resend/{{submissionId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-submission.md) for the provider-specific parameters and requirements.

