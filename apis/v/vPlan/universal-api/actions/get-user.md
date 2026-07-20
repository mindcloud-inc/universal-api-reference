# vPlan: Get User



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-user?connectionId=$CONNECTION_ID&id=4ec32e39-fe3c-4db8-9321-410b2fd68c8b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "4ec32e39-fe3c-4db8-9321-410b2fd68c8b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | User identifier. Default: `4ec32e39-fe3c-4db8-9321-410b2fd68c8b`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived_at": "string",
      "avatar": "string",
      "avatar_checksum": "string",
      "avatar_signature": "string",
      "card_visibility": "string",
      "created_at": "string",
      "deleted_at": "string",
      "display_name": "Ava Chen",
      "email": "ava@example.com",
      "external_ref": "string",
      "fullname": "Ava Chen",
      "id": "string",
      "idp_id": "string",
      "invite_id": "string",
      "is_sso": true,
      "language": "string",
      "mfa_enabled": true,
      "mobile": "string",
      "notify_own_changes": true,
      "resource_id": "string",
      "role": "string",
      "status": "string",
      "timezone": "string",
      "updated_at": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived_at` | string | Archive timestamp. |
| `avatar` | string | Avatar URL. |
| `avatar_checksum` | string | Avatar checksum. |
| `avatar_signature` | string | Avatar signature. |
| `card_visibility` | string | Card visibility scope. |
| `created_at` | string | Creation timestamp. |
| `deleted_at` | string | Deletion timestamp. |
| `display_name` | string | Display name. |
| `email` | string | Email address. |
| `external_ref` | string | External reference. |
| `fullname` | string | Full name. |
| `id` | string | User identifier. |
| `idp_id` | string | Identity provider identifier. |
| `invite_id` | string | Invite identifier. |
| `is_sso` | boolean | Whether SSO is enabled. |
| `language` | string | Preferred language. |
| `mfa_enabled` | boolean | Whether MFA is enabled. |
| `mobile` | string | Mobile number. |
| `notify_own_changes` | boolean | Whether own changes trigger notifications. |
| `resource_id` | string | Linked resource identifier. |
| `role` | string | User role. |
| `status` | string | User status. |
| `timezone` | string | Timezone. |
| `updated_at` | string | Last update timestamp. |
| `username` | string | Username. |

## Native endpoint

Through the native vPlan API, this operation is `GET /user/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

