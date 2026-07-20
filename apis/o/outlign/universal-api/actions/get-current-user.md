# Outlign: Get Current User

Retrieves the current authenticated user from Outlign.

```
GET https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": {},
      "avatarUrl": {},
      "capacity": {},
      "colour": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "emailNotificationFrequency": "ava@example.com",
      "emailVerifiedAt": {},
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "isDemo": true,
      "isGuest": 1,
      "lastName": "Chen",
      "position": "string",
      "timezone": "string",
      "twoFactorRecoveryCodes": {},
      "twoFactorSecret": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | object |  |
| `avatarUrl` | object |  |
| `capacity` | object |  |
| `colour` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `emailNotificationFrequency` | string |  |
| `emailVerifiedAt` | object |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `isDemo` | boolean |  |
| `isGuest` | number |  |
| `lastName` | string |  |
| `position` | string |  |
| `timezone` | string |  |
| `twoFactorRecoveryCodes` | object |  |
| `twoFactorSecret` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Outlign API, this operation is `GET /me` (base URL `https://go.outlign.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

