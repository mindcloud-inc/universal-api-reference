# Frontegg: Create User

Creates a new user in Frontegg.

```
POST https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tenantId": "string",
  "email": "ava@example.com",
  "name": "Ava Chen",
  "roleIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tenantId": "string",
    "email": "ava@example.com",
    "name": "Ava Chen",
    "roleIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantId` | string | yes | Tenant ID that the user belongs to. |
| `email` | string | yes | User email address. |
| `name` | string | yes | Full name for the user. |
| `roleIds[]` | array<string> | yes | Role IDs to assign to the user. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `password` | string | no | Optional password for the new user. |
| `username` | string | no | Optional username when email is omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activatedForTenant": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "isLocked": true,
      "managedBy": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "profilePictureUrl": "https://example.com",
      "provider": "string",
      "sub": "string",
      "tenantId": "string",
      "tenantIds": [
        "string"
      ],
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activatedForTenant` | boolean | Whether the user is active for the tenant. |
| `createdAt` | date | Creation timestamp. |
| `email` | string | User email address. |
| `id` | string | User ID. |
| `isLocked` | boolean | Whether the user is locked. |
| `managedBy` | string | User management source. |
| `name` | string | User display name. |
| `phoneNumber` | string | Phone number when present. |
| `profilePictureUrl` | string | Profile picture URL. |
| `provider` | string | Authentication provider. |
| `sub` | string | Subject identifier. |
| `tenantId` | string | Primary tenant ID. |
| `tenantIds` | array<string> | Tenant IDs assigned to the user. |
| `verified` | boolean | Whether the user is verified. |

## Native endpoint

Through the native Frontegg API, this operation is `POST /identity/resources/vendor-only/users/v1` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

