# WorkOS: Deactivate an organization membership

Deactivates an organization membership in your WorkOS environment.

```
PUT https://connect.mindcloud.co/v1/universal/workOS/latest/actions/deactivate-an-organization-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/deactivate-an-organization-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workOS/latest/actions/deactivate-an-organization-membership', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique ID of the organization membership. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_attributes": {},
      "directory_managed": true,
      "id": "string",
      "message": "string",
      "object": "string",
      "organization_id": "string",
      "organization_name": "Ava Chen",
      "role": {},
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | An ISO 8601 timestamp. |
| `custom_attributes` | object | An object containing IdP-sourced attributes from the linked [Directory User](/reference/directory-sync/directory-user) or [SSO Profile](/reference/sso/profile). Directory User attributes take precedence when both are linked. |
| `directory_managed` | boolean | Whether this organization membership is managed by a directory sync connection. |
| `id` | string | The unique ID of the organization membership. |
| `message` | string | WorkOS response field message. |
| `object` | string | Distinguishes the organization membership object. |
| `organization_id` | string | The ID of the organization which the user belongs to. |
| `organization_name` | string | The name of the organization which the user belongs to. |
| `role` | object | The primary role assigned to the user within the organization. |
| `status` | string | The status of the organization membership. One of `active`, `inactive`, or `pending`. |
| `updated_at` | date | An ISO 8601 timestamp. |
| `user_id` | string | The ID of the user. |

## Native endpoint

Through the native WorkOS API, this operation is `PUT /user_management/organization_memberships/{id}/deactivate` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deactivate-an-organization-membership.md) for the provider-specific parameters and requirements.

