# Formstack: Get Submission

Retrieves details for a submission from Formstack.

```
GET https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-submission?connectionId=$CONNECTION_ID&submissionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-submission?${params}`, {
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
| `submissionId` | number | yes | The unique identifier of the submission to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalStatus": "string",
      "data": [
        {}
      ],
      "formId": 1,
      "id": 1,
      "latitude": "string",
      "longitude": "string",
      "paymentStatus": "string",
      "portal": {},
      "prettyFieldId": 1,
      "remoteAddr": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "userAgent": "string",
      "workflow": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalStatus` | string | The current approval status when approvals are enabled. |
| `data` | array<object> | Array of field data contained in the submission. |
| `formId` | number | The ID of the form this submission belongs to. |
| `id` | number | The ID of the submission. |
| `latitude` | string | The GPS latitude coordinate if location data was captured. |
| `longitude` | string | The GPS longitude coordinate if location data was captured. |
| `paymentStatus` | string | The current payment status if the form includes payment processing. |
| `portal` | object | Portal information returned by the API for this submission. |
| `prettyFieldId` | number | The field ID used to generate a human-readable name for this submission. |
| `remoteAddr` | string | The IP address from which the submission was made. |
| `timestamp` | date | The date and time when the submission was created. |
| `userAgent` | string | The browser user agent string of the submitter. |
| `workflow` | object | Workflow information returned by the API for this submission. |

## Native endpoint

Through the native Formstack API, this operation is `GET /submissions/:submissionId` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission.md) for the provider-specific parameters and requirements.

