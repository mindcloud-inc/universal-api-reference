# WorkOS: Check authorization

Checks authorization in your WorkOS environment.

```
POST https://connect.mindcloud.co/v1/universal/workOS/latest/actions/check-authorization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/check-authorization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organization_membership_id": "string",
  "permission_slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workOS/latest/actions/check-authorization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organization_membership_id": "string",
    "permission_slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organization_membership_id` | string | yes | The ID of the organization membership to check. |
| `permission_slug` | string | yes | The slug of the permission to check. |
| `resource_id` | string | no | The ID of the resource. |
| `resource_external_id` | string | no | The external ID of the resource. |
| `resource_type_slug` | string | no | The slug of the resource type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorized": true,
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
| `authorized` | boolean | Whether the organization membership has the specified permission on the resource. |
| `id` | string | WorkOS response field id. |
| `message` | string | WorkOS response field message. |
| `object` | string | WorkOS response field object. |

## Native endpoint

Through the native WorkOS API, this operation is `POST /authorization/organization_memberships/{organization_membership_id}/check` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-authorization.md) for the provider-specific parameters and requirements.

