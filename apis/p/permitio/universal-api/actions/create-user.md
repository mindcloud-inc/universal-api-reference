# Permit.io: Create User



```
POST https://connect.mindcloud.co/v1/universal/permitio/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projId": "string",
  "envId": "string",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/permitio/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projId": "string",
    "envId": "string",
    "key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projId` | string | yes | Permit project identifier or key. |
| `envId` | string | yes | Permit environment identifier or key. |
| `key` | string | yes | Unique user key within the Permit environment. |
| `email` | string | no | User email address. |
| `firstName` | string | no | User first name. |
| `lastName` | string | no | User last name. |
| `attributes` | object | no | Custom user attributes object. |
| `roleAssignments[]` | array<object> | no | Initial role assignments array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associatedTenants": [
        {}
      ],
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "environmentId": "string",
      "firstName": "Ava",
      "id": "string",
      "key": "string",
      "lastName": "Chen",
      "organizationId": "string",
      "projectId": "string",
      "roles": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associatedTenants` | array<object> |  |
| `attributes` | object |  |
| `createdAt` | date |  |
| `email` | string |  |
| `environmentId` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `key` | string |  |
| `lastName` | string |  |
| `organizationId` | string |  |
| `projectId` | string |  |
| `roles` | array<object> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Permit.io API, this operation is `POST /v2/facts/:projId/:envId/users` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

