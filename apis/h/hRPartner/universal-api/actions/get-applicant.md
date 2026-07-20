# HR Partner: Get Applicant



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-applicant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-applicant?connectionId=$CONNECTION_ID&applicantID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicantID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-applicant?${params}`, {
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
| `applicantID` | string | yes | Applicant ID from HR Partner. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstNames": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "jobApplications": [
        {}
      ],
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstNames` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `jobApplications` | array<object> |  |
| `lastName` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /applicant/:applicantID` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-applicant.md) for the provider-specific parameters and requirements.

