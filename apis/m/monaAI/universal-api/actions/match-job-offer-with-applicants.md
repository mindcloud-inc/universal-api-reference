# Mona AI: Match Job Offer With Applicants

Matches a job offer with applicants in Mona AI.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/match-job-offer-with-applicants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/match-job-offer-with-applicants?connectionId=$CONNECTION_ID&applicantObjects%5B%5D=%5Bobject%20Object%5D&jobOfferObject=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicantObjects[]": "[object Object]",
  "jobOfferObject": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/match-job-offer-with-applicants?${params}`, {
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
| `applicantObjects[]` | array<object> | yes | Applicant objects to match against the job offer. |
| `brandingInfo` | object | no | Optional branding information object. |
| `businessName` | string | no | Business name used for matching context. |
| `cvData` | string | no | CV data used for matching. |
| `jobOfferObject` | object | yes | Job offer object to match against multiple applicants. |
| `logs[]` | array<object> | no | Optional matching logs array. |
| `profileType` | string | no | Profile type used for matching context. |
| `profileURL` | string | no | Profile URL used for matching context. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mona AI API returns.

## Native endpoint

Through the native Mona AI API, this operation is `POST /matching/jobOfferWithMultipleApplicants` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/match-job-offer-with-applicants.md) for the provider-specific parameters and requirements.

