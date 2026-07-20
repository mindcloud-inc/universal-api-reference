# Cryptlex: Create User

Creates a user in Cryptlex.

```
POST https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "password": "string",
  "role": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava",
    "password": "string",
    "role": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address for the user. |
| `firstName` | string | yes | First name for the user. |
| `password` | string | yes | Password for the user. |
| `lastName` | string | no | Last name for the user. |
| `company` | string | no | Company name for the user. |
| `role` | string | yes | Role assigned to the user. |
| `allowCustomerPortalAccess` | boolean | no | Whether the user can access the customer portal. |
| `tags[]` | array<string> | no | Tags to attach to the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowCustomerPortalAccess": true,
      "company": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "lastLoginAt": "2026-05-07T12:00:00.000Z",
      "lastSeenAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "role": "string",
      "twoFactorEnabled": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowCustomerPortalAccess` | boolean |  |
| `company` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `lastLoginAt` | date |  |
| `lastSeenAt` | date |  |
| `name` | string |  |
| `role` | string |  |
| `twoFactorEnabled` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Cryptlex API, this operation is `POST /v3/users` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

