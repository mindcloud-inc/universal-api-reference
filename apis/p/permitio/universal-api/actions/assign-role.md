# Permit.io: Assign Role



```
POST https://connect.mindcloud.co/v1/universal/permitio/latest/actions/assign-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/assign-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projId": "string",
  "envId": "string",
  "role": "string",
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/permitio/latest/actions/assign-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projId": "string",
    "envId": "string",
    "role": "string",
    "user": "string"
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
| `role` | string | yes | Role key to assign. |
| `user` | string | yes | User key receiving the assignment. |
| `tenant` | string | no | Tenant receiving the assignment, when applicable. |
| `resourceInstance` | string | no | Resource instance receiving the assignment, when applicable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "environmentId": "string",
      "id": "string",
      "organizationId": "string",
      "projectId": "string",
      "resourceInstance": "string",
      "resourceInstanceId": "string",
      "role": "string",
      "roleId": "string",
      "tenant": "string",
      "tenantId": "string",
      "user": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `environmentId` | string |  |
| `id` | string |  |
| `organizationId` | string |  |
| `projectId` | string |  |
| `resourceInstance` | string |  |
| `resourceInstanceId` | string |  |
| `role` | string |  |
| `roleId` | string |  |
| `tenant` | string |  |
| `tenantId` | string |  |
| `user` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Permit.io API, this operation is `POST /v2/facts/:projId/:envId/role_assignments` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-role.md) for the provider-specific parameters and requirements.

