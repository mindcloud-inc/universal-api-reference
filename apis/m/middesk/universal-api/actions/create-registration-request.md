# Middesk: Create a registration request

Creates a registration request in Middesk.

```
POST https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-registration-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-registration-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "email": "ava@example.com",
  "state": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-registration-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string",
    "email": "ava@example.com",
    "state": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | Existing Middesk company ID to associate with the registration request. |
| `companyName` | string | no | Company name used to create the registration request when no company ID is provided. |
| `email` | string | yes | Email address of the applicant or contact. |
| `state` | string | yes | US state where the registration request is being created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agencies": [
        {}
      ],
      "companyId": "string",
      "createdAt": "string",
      "externalId": "string",
      "id": "string",
      "inviteLink": "https://example.com",
      "items": [
        {}
      ],
      "object": "string",
      "state": "string",
      "status": "string",
      "submittedAt": "string",
      "taxRegistration": {},
      "taxRegistrationTypes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agencies` | array<object> |  |
| `companyId` | string |  |
| `createdAt` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `inviteLink` | string |  |
| `items` | array<object> |  |
| `object` | string |  |
| `state` | string |  |
| `status` | string |  |
| `submittedAt` | string |  |
| `taxRegistration` | object |  |
| `taxRegistrationTypes` | array<string> |  |

## Native endpoint

Through the native Middesk API, this operation is `POST /partner/registration_requests` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-registration-request.md) for the provider-specific parameters and requirements.

