# HoorayHR: Get User

Retrieves an employee record from HoorayHR.

```
GET https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoorayHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-user?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-user?${params}`, {
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
| `id` | number | yes | The user ID to retrieve. |

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

Through the native HoorayHR API, this operation is `GET /users/:id` (base URL `https://api.hoorayhr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

