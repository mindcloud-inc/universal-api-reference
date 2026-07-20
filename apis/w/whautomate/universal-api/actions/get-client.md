# Whautomate: Get Client

Retrieves a client from Whautomate.

```
GET https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whautomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/get-client?${params}`, {
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
| `clientId` | string | yes |  |

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

Through the native Whautomate API, this operation is `GET /v1/clients/{{clientId}}` (base URL `https://api.whautomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

