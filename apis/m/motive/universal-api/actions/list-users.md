# Motive: List users



```
GET https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Motive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-users?${params}`, {
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
| `role` | string | no | Filter users by role. |
| `dutyStatus` | string | no | Filter drivers by duty status. |
| `status` | string | no | Filter users by status. |
| `name` | string | no | Filter users by first name, last name, or both. |
| `updatedAfter` | date | no | Return users updated after the given date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyReferenceId": {},
      "createdAt": "string",
      "email": "ava@example.com",
      "expiresAt": {},
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "metricUnits": true,
      "mobileCurrentSignInAt": {},
      "mobileLastActiveAt": {},
      "mobileLastSignInAt": {},
      "phone": "string",
      "phone2": {},
      "phoneCountryCode": "string",
      "phoneCountryCode2": {},
      "phoneExt": "string",
      "role": "string",
      "status": "string",
      "timeZone": "string",
      "updatedAt": "string",
      "webCurrentSignInAt": "string",
      "webLastActiveAt": "string",
      "webLastSignInAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyReferenceId` | object |  |
| `createdAt` | string |  |
| `email` | string |  |
| `expiresAt` | object |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `metricUnits` | boolean |  |
| `mobileCurrentSignInAt` | object |  |
| `mobileLastActiveAt` | object |  |
| `mobileLastSignInAt` | object |  |
| `phone` | string |  |
| `phone2` | object |  |
| `phoneCountryCode` | string |  |
| `phoneCountryCode2` | object |  |
| `phoneExt` | string |  |
| `role` | string |  |
| `status` | string |  |
| `timeZone` | string |  |
| `updatedAt` | string |  |
| `webCurrentSignInAt` | string |  |
| `webLastActiveAt` | string |  |
| `webLastSignInAt` | string |  |

## Native endpoint

Through the native Motive API, this operation is `GET /v1/users` (base URL `https://api.gomotive.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

