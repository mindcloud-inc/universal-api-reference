# WorkOS: Create an organization membership

Creates an organization membership in your WorkOS environment.

```
POST https://connect.mindcloud.co/v1/universal/workOS/latest/actions/create-an-organization-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/create-an-organization-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user_id": "string",
  "organization_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workOS/latest/actions/create-an-organization-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user_id": "string",
    "organization_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user_id` | string | yes | The ID of the [user](/reference/authkit/user). |
| `organization_id` | string | yes | The ID of the [organization](/reference/organization) which the user belongs to. |
| `role_slug` | string | no | A single role identifier. Defaults to `member` or the explicit default role. Mutually exclusive with `role_slugs`. |
| `role_slugs` | list<string> | no | An array of role identifiers. Limited to one role when Multiple Roles is disabled. Mutually exclusive with `role_slug`. |

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

Through the native WorkOS API, this operation is `POST /user_management/organization_memberships` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-an-organization-membership.md) for the provider-specific parameters and requirements.

