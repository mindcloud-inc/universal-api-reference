# Tally: List Users



```
GET https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tally `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-users?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-users?${params}`, {
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
| `organizationId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticationMethodsCount": 1,
      "avatarUrl": "https://example.com",
      "createdAt": "string",
      "email": "ava@example.com",
      "emailDomain": {},
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "hasPasswordSet": true,
      "hasTwoFactorEnabled": true,
      "id": "string",
      "isBlocked": true,
      "isDeleted": true,
      "isUnknownDeviceVerificationDisabled": true,
      "lastName": "Chen",
      "organizationId": "string",
      "ssoIsConnectedWithApple": true,
      "ssoIsConnectedWithGoogle": true,
      "timezone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticationMethodsCount` | number |  |
| `avatarUrl` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `emailDomain` | object |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `hasPasswordSet` | boolean |  |
| `hasTwoFactorEnabled` | boolean |  |
| `id` | string |  |
| `isBlocked` | boolean |  |
| `isDeleted` | boolean |  |
| `isUnknownDeviceVerificationDisabled` | boolean |  |
| `lastName` | string |  |
| `organizationId` | string |  |
| `ssoIsConnectedWithApple` | boolean |  |
| `ssoIsConnectedWithGoogle` | boolean |  |
| `timezone` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Tally API, this operation is `GET organizations/:organizationId/users` (base URL `https://api.tally.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

