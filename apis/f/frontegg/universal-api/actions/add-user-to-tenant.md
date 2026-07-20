# Frontegg: Add User To Tenant

Adds a user to an account in Frontegg.

```
PUT https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/add-user-to-tenant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/add-user-to-tenant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "tenantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/add-user-to-tenant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "tenantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | User ID to add to a tenant. |
| `tenantId` | string | yes | Tenant ID to add the user to. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skipInviteEmail` | boolean | no | Skip the invitation email when true. |
| `validateTenantExist` | boolean | no | Validate the tenant before adding the user. |

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
      "tenantId": "string",
      "tenantIds": [
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
| `activatedForTenant` | boolean | Whether the user is active for the tenant. |
| `createdAt` | date | Creation timestamp. |
| `email` | string | User email address. |
| `id` | string | User ID. |
| `isLocked` | boolean | Whether the user is locked. |
| `managedBy` | string | User management source. |
| `name` | string | User display name. |
| `tenantId` | string | Primary tenant ID. |
| `tenantIds` | array<string> | All tenant IDs assigned to the user. |

## Native endpoint

Through the native Frontegg API, this operation is `POST /identity/resources/users/v1/:userId/tenant` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-tenant.md) for the provider-specific parameters and requirements.

