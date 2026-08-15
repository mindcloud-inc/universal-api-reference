# Google Ads: Add Lead Feedback



```
POST https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/add-lead-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/add-lead-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyAnswer": "string",
  "customerId": "string",
  "leadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/add-lead-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyAnswer": "string",
    "customerId": "string",
    "leadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyAnswer` | list<string> | yes |  |
| `surveyDissatisfied.otherReasonComment` | string | no |  |
| `surveySatisfied.otherReasonComment` | string | no |  |
| `surveyDissatisfied` | object | no |  |
| `surveyDissatisfied.surveyDissatisfiedReason` | list<string> | no |  |
| `surveySatisfied` | object | no |  |
| `surveySatisfied.surveySatisfiedReason` | list<string> | no |  |
| `customerId` | list | yes |  |
| `leadId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditIssuanceDecision": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditIssuanceDecision` | string | Bonus credit issuance decision returned after providing lead feedback. |

## Native endpoint

Through the native Google Ads API, this operation is `POST v21/customers/:customerId/localServicesLeads/:leadId:provideLeadFeedback` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-lead-feedback.md) for the provider-specific parameters and requirements.

