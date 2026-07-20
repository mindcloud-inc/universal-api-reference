# Moxie: Create Form Submission

Creates a new form submission in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-form-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-form-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-form-submission', {
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
| `formName` | string | no | Form name to submit. |
| `firstName` | string | no | Lead first name. |
| `lastName` | string | no | Lead last name. |
| `email` | string | no | Lead email address. |
| `phone` | string | no | Lead phone number. |
| `businessName` | string | no | Business name from the form submission. |
| `pipelineStageName` | string | no | Pipeline stage name for the submission. |
| `answers` | list<object> | no | List of answer objects for form questions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "clientId": "string",
      "files": [
        {}
      ],
      "formData": {},
      "formName": "Ava Chen",
      "id": "string",
      "ipLookup": {},
      "isDiscovery": true,
      "leadGenArchived": true,
      "notes": "string",
      "opportunityId": "string",
      "privateSubmission": true,
      "submissionToken": "string",
      "submittedAt": "2026-05-07T12:00:00.000Z",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `clientId` | string |  |
| `files` | array<object> |  |
| `formData` | object |  |
| `formName` | string |  |
| `id` | string |  |
| `ipLookup` | object |  |
| `isDiscovery` | boolean |  |
| `leadGenArchived` | boolean |  |
| `notes` | string |  |
| `opportunityId` | string |  |
| `privateSubmission` | boolean |  |
| `submissionToken` | string |  |
| `submittedAt` | date |  |
| `summary` | string |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/formSubmissions/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form-submission.md) for the provider-specific parameters and requirements.

