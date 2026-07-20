# WorkOS: Get an invitation

Retrieves an invitation from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-an-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-an-invitation?connectionId=$CONNECTION_ID&id=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-an-invitation?${params}`, {
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
| `id` | string | yes | The unique ID of the invitation. |
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

Through the native WorkOS API, this operation is `GET /user_management/invitations/{id}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-invitation.md) for the provider-specific parameters and requirements.

