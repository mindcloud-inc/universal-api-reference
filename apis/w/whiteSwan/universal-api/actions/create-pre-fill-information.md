# White Swan: Create Pre-Fill Information

Creates application pre-fill information in White Swan.

```
POST https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/create-pre-fill-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a White Swan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/create-pre-fill-information" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/create-pre-fill-information', {
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
| `requestsIds[]` | array<string> | no | Plan request IDs to attach this pre-fill payload to. |
| `firstName` | string | no | Applicant first name. |
| `middleName` | string | no | Applicant middle name. |
| `lastName` | string | no | Applicant last name. |
| `gender` | string | no | Applicant gender. |
| `dateOfBirth` | string | no | Applicant date of birth in White Swan format. |
| `phone` | string | no | Applicant phone number. |
| `email` | string | no | Applicant email address. |
| `address` | string | no | Applicant mailing address. |
| `maritalStatus` | string | no | Applicant marital status. |
| `ownerEstimatedIncome` | number | no | Estimated annual income for the owner. |
| `householdTotalAssets` | number | no | Total household assets. |

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

Through the native White Swan API, this operation is `POST /new_prefill_info` (base URL `https://app.whiteswan.io/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pre-fill-information.md) for the provider-specific parameters and requirements.

