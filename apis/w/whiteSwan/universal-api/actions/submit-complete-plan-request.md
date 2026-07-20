# White Swan: Submit Complete Plan Request

Submits a complete personal plan request in White Swan.

```
POST https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/submit-complete-plan-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a White Swan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/submit-complete-plan-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/submit-complete-plan-request', {
  method: 'POST',
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
| `name` | string | no | Applicant full name. |
| `email` | string | no | Applicant email address. |
| `phone` | string | no | Applicant phone number. |
| `policyType` | string | no | Requested policy type. |
| `mainGoal` | string | no | Primary plan goal. |
| `residentState` | string | no | Applicant resident state. |
| `deathBenefit` | number | no | Requested death benefit. |
| `paymentSchedule` | string | no | Preferred payment schedule. |
| `termDuration` | string | no | Requested term duration. |
| `gender` | string | no | Applicant gender. |
| `healthRating` | string | no | Underwriting health rating. |
| `dateOfBirth` | string | no | Applicant date of birth in White Swan format. |
| `tobacco` | boolean | no | Whether the applicant uses tobacco. |
| `marijuana` | boolean | no | Whether the applicant uses marijuana. |
| `heightFeet` | number | no | Applicant height in feet. |
| `heightInches` | number | no | Applicant remaining height in inches. |
| `weightPounds` | number | no | Applicant weight in pounds. |
| `convertability` | boolean | no | Whether the term should be convertible. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object |  |
| `status` | string |  |

## Native endpoint

Through the native White Swan API, this operation is `POST /complete_request` (base URL `https://app.whiteswan.io/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-complete-plan-request.md) for the provider-specific parameters and requirements.

