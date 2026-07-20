# CallRail: Create Form Submission

Creates a form submission in CallRail.

```
POST https://connect.mindcloud.co/v1/universal/callRail/latest/actions/create-form-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/create-form-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account_id": "string",
  "form_submission.company_id": "string",
  "form_submission.form_url": "https://example.com",
  "form_submission.form_data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callRail/latest/actions/create-form-submission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account_id": "string",
    "form_submission.company_id": "string",
    "form_submission.form_url": "https://example.com",
    "form_submission.form_data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account_id` | string | yes |  |
| `form_submission.company_id` | string | yes |  |
| `form_submission.form_url` | string | yes |  |
| `form_submission.form_data` | object | yes |  |
| `form_submission.referrer` | string | no |  |
| `form_submission.referring_url` | string | no |  |
| `form_submission.landing_page_url` | string | no |  |
| `form_submission.session_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "firstForm": true,
      "formData": {
        "emailAddress": "ava@example.com",
        "message": "string",
        "phoneNumber": "string",
        "textingConsent": "string",
        "yourName": "Ava Chen"
      },
      "formUrl": "https://example.com",
      "id": "string",
      "landingPageUrl": "https://example.com",
      "personId": "string",
      "referrer": "string",
      "referringUrl": "https://example.com",
      "submittedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `firstForm` | boolean |  |
| `formData` | object |  |
| `formData.emailAddress` | string |  |
| `formData.message` | string |  |
| `formData.phoneNumber` | string |  |
| `formData.textingConsent` | string |  |
| `formData.yourName` | string |  |
| `formUrl` | string |  |
| `id` | string |  |
| `landingPageUrl` | string |  |
| `personId` | string |  |
| `referrer` | string |  |
| `referringUrl` | string |  |
| `submittedAt` | string |  |

## Native endpoint

Through the native CallRail API, this operation is `POST /v3/a/:account_id/form_submissions.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form-submission.md) for the provider-specific parameters and requirements.

