# HoorayHR: List Users

Retrieves employee records from the HoorayHR directory.

```
GET https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoorayHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-users?${params}`, {
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
| `includeExtraFields` | boolean | no | Whether to include user extra fields in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "civilStatus": "string",
      "companyId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "email": "ava@example.com",
      "entityId": 1,
      "firstName": "Ava",
      "gender": "string",
      "holidayPolicyId": 1,
      "id": 1,
      "isAdmin": 1,
      "isDemoData": true,
      "lastName": "Chen",
      "lastNameUsage": "Chen",
      "locale": "string",
      "nationality": "string",
      "status": 1,
      "timezone": "string",
      "travelAllowance": 1,
      "travelAllowanceCurrency": "string",
      "twoFactorAuthentication": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `civilStatus` | string |  |
| `companyId` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `email` | string |  |
| `entityId` | number |  |
| `firstName` | string |  |
| `gender` | string |  |
| `holidayPolicyId` | number |  |
| `id` | number |  |
| `isAdmin` | number |  |
| `isDemoData` | boolean |  |
| `lastName` | string |  |
| `lastNameUsage` | string |  |
| `locale` | string |  |
| `nationality` | string |  |
| `status` | number |  |
| `timezone` | string |  |
| `travelAllowance` | number |  |
| `travelAllowanceCurrency` | string |  |
| `twoFactorAuthentication` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native HoorayHR API, this operation is `GET /users` (base URL `https://api.hoorayhr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

