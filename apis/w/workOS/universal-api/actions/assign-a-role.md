# WorkOS: Assign a role

Assigns a role in your WorkOS environment.

```
POST https://connect.mindcloud.co/v1/universal/workOS/latest/actions/assign-a-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/assign-a-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organization_membership_id": "string",
  "role_slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workOS/latest/actions/assign-a-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organization_membership_id": "string",
    "role_slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organization_membership_id` | string | yes | The ID of the organization membership. |
| `role_slug` | string | yes | The slug of the role to assign. |
| `resource_id` | string | no | The ID of the resource. Use either this or `resource_external_id` and `resource_type_slug`. |
| `resource_external_id` | string | no | The external ID of the resource. Requires `resource_type_slug`. |
| `resource_type_slug` | string | no | The resource type slug. Required with `resource_external_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "message": "string",
      "object": "string",
      "resource": {},
      "role": {},
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | An ISO 8601 timestamp. |
| `id` | string | Unique identifier of the role assignment. |
| `message` | string | WorkOS response field message. |
| `object` | string | Distinguishes the role assignment object. |
| `resource` | object | The resource to which the role is assigned. |
| `role` | object | The role included in the assignment. |
| `updated_at` | date | An ISO 8601 timestamp. |

## Native endpoint

Through the native WorkOS API, this operation is `POST /authorization/organization_memberships/{organization_membership_id}/role_assignments` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-a-role.md) for the provider-specific parameters and requirements.

