# CallRail: Update Form Submission

Updates a form submission in CallRail.

```
PUT https://connect.mindcloud.co/v1/universal/callRail/latest/actions/update-form-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/update-form-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account_id": "string",
  "form_submission_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callRail/latest/actions/update-form-submission', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account_id": "string",
    "form_submission_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account_id` | string | yes |  |
| `form_submission_id` | string | yes |  |
| `tags[]` | array<string> | no |  |
| `append_tags` | boolean | no |  |
| `lead_status` | string | no |  |
| `value` | string | no |  |
| `note` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": "string",
      "companyId": "string",
      "customerEmail": "ava@example.com",
      "customerName": "Ava Chen",
      "customerPhoneNumber": "string",
      "firstForm": true,
      "formattedCustomerName": "Ava Chen",
      "formattedCustomerPhoneNumber": "string",
      "formData": {
        "emailAddress": "ava@example.com",
        "message": "string",
        "phoneNumber": "string",
        "textingConsent": "string",
        "yourName": "Ava Chen"
      },
      "formUrl": "https://example.com",
      "id": "string",
      "keywords": "string",
      "landingPageUrl": "https://example.com",
      "medium": "string",
      "personId": "string",
      "referrer": "string",
      "referringUrl": "https://example.com",
      "source": "string",
      "submittedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | string |  |
| `companyId` | string |  |
| `customerEmail` | string |  |
| `customerName` | string |  |
| `customerPhoneNumber` | string |  |
| `firstForm` | boolean |  |
| `formattedCustomerName` | string |  |
| `formattedCustomerPhoneNumber` | string |  |
| `formData` | object |  |
| `formData.emailAddress` | string |  |
| `formData.message` | string |  |
| `formData.phoneNumber` | string |  |
| `formData.textingConsent` | string |  |
| `formData.yourName` | string |  |
| `formUrl` | string |  |
| `id` | string |  |
| `keywords` | string |  |
| `landingPageUrl` | string |  |
| `medium` | string |  |
| `personId` | string |  |
| `referrer` | string |  |
| `referringUrl` | string |  |
| `source` | string |  |
| `submittedAt` | string |  |

## Native endpoint

Through the native CallRail API, this operation is `PUT /v3/a/:account_id/form_submissions/:form_submission_id.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-submission.md) for the provider-specific parameters and requirements.

