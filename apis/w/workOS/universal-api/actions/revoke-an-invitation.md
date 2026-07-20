# WorkOS: Revoke an invitation

Revokes an invitation in your WorkOS environment.

```
POST https://connect.mindcloud.co/v1/universal/workOS/latest/actions/revoke-an-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/revoke-an-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workOS/latest/actions/revoke-an-invitation', {
  method: 'POST',
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
| `id` | string | yes | The unique ID of the invitation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accepted_at": "2026-05-07T12:00:00.000Z",
      "accepted_user_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "inviter_user_id": "string",
      "message": "string",
      "object": "string",
      "organization_id": "string",
      "revoked_at": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "token": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepted_at` | date | The timestamp when the invitation was accepted, or null if not yet accepted. |
| `accepted_user_id` | string | The ID of the user who accepted the invitation, once accepted. |
| `created_at` | date | An ISO 8601 timestamp. |
| `email` | string | The email address of the recipient. |
| `expires_at` | date | The timestamp when the invitation expires. |
| `id` | string | The unique ID of the invitation. |
| `inviter_user_id` | string | The ID of the user who invited the recipient, if provided. |
| `message` | string | WorkOS response field message. |
| `object` | string | Distinguishes the invitation object. |
| `organization_id` | string | The ID of the [organization](/reference/organization) that the recipient will join. |
| `revoked_at` | date | The timestamp when the invitation was revoked, or null if not revoked. |
| `state` | string | The state of the invitation. |
| `token` | string | The token used to accept the invitation. |
| `updated_at` | date | An ISO 8601 timestamp. |

## Native endpoint

Through the native WorkOS API, this operation is `POST /user_management/invitations/{id}/revoke` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-an-invitation.md) for the provider-specific parameters and requirements.

