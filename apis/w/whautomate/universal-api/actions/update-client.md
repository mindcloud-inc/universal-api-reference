# Whautomate: Update Client

Updates an existing client in Whautomate.

```
PUT https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whautomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes |  |
| `contactType` | string | no |  |
| `countryCode` | string | no |  |
| `email` | string | no |  |
| `fullName` | string | no |  |
| `phone` | string | no |  |
| `preferredName` | string | no |  |
| `primaryLocation` | object | no |  |
| `tags[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "addressType": "string",
      "clientId": "string",
      "company": {},
      "contactType": "string",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emergencyName": "Ava Chen",
      "emergencyPhone": "string",
      "emergencyRelationType": "string",
      "fullName": "Ava Chen",
      "gender": "string",
      "id": "string",
      "identificationNumber": "string",
      "maritalStatus": "string",
      "notes": "string",
      "phone": "string",
      "preferredLanguage": "string",
      "preferredName": "Ava Chen",
      "primaryLocation": {},
      "referralSource": "string",
      "registrationDate": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "taxIdNumber": "string",
      "taxIdType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `addressType` | string |  |
| `clientId` | string |  |
| `company` | object |  |
| `contactType` | string |  |
| `countryCode` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `emergencyName` | string |  |
| `emergencyPhone` | string |  |
| `emergencyRelationType` | string |  |
| `fullName` | string |  |
| `gender` | string |  |
| `id` | string |  |
| `identificationNumber` | string |  |
| `maritalStatus` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `preferredLanguage` | string |  |
| `preferredName` | string |  |
| `primaryLocation` | object |  |
| `referralSource` | string |  |
| `registrationDate` | date |  |
| `tags` | array<string> |  |
| `taxIdNumber` | string |  |
| `taxIdType` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Whautomate API, this operation is `PUT /v1/clients/{{clientId}}` (base URL `https://api.whautomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

