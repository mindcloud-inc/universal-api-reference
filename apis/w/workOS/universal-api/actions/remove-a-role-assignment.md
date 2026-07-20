# WorkOS: Remove a role assignment

Removes a role assignment from your WorkOS environment.

```
DELETE https://connect.mindcloud.co/v1/universal/workOS/latest/actions/remove-a-role-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/remove-a-role-assignment?connectionId=$CONNECTION_ID&organization_membership_id=string&role_slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization_membership_id": "string",
  "role_slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/remove-a-role-assignment?${params}`, {
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
| `organization_membership_id` | string | yes | The ID of the organization membership. |
| `role_slug` | string | yes | The slug of the role to remove. |
| `resource_id` | string | no | The ID of the resource. Use either this or `resource_external_id` and `resource_type_slug`. |
| `resource_external_id` | string | no | The external ID of the resource. Requires `resource_type_slug`. |
| `resource_type_slug` | string | no | The resource type slug. Required with `resource_external_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | WorkOS response field id. |
| `message` | string | WorkOS response field message. |
| `object` | string | WorkOS response field object. |

## Native endpoint

Through the native WorkOS API, this operation is `DELETE /authorization/organization_memberships/{organization_membership_id}/role_assignments` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-a-role-assignment.md) for the provider-specific parameters and requirements.

