# Accept or ignore a received invitation with ConnectSafely

Accepts or ignores a received invitation on LinkedIn. Works for all invitation types: connection requests, organization follows, newsletter subscriptions, and events. Use the data from GET /invitations/received to populate the required fields.

## Endpoint

- **Method:** `POST`
- **Path:** `/invitations/received/respond`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Accept or ignore a received invitation](https://connectsafely.ai/docs/api/linkedin-actions/post-invitations-received-respond-respond-to-received-invitation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `action` | body | `list` | yes | Action to perform on the invitation Accepted values: `ACCEPT`, `IGNORE`. |
| `invitationId` | body | `string` | yes | LinkedIn invitation ID from the received invitation |
| `validationToken` | body | `string` | yes | Validation token from the received invitation |
| `linkedInInvitationType` | body | `string` | yes | LinkedIn invitation type (e.g., GenericInvitationType_CONNECTION, GenericInvitationType_ORGANIZATION) |
| `firstName` | body | `string` | yes | First name of the inviter |
| `lastName` | body | `string` | yes | Last name of the inviter |
| `profileId` | body | `string` | no | LinkedIn member ID (ACoAAA format). Optional, required for connection invitations. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` | Whether the action was successful |
| `message` | `string` | Success message with action details |
| `accountId` | `string` | LinkedIn account ID used |

### Example response

```json
{
  "success": true,
  "message": "Invitation from Deepika Khare accepted",
  "accountId": "69da1eacf365891afa0426a4"
}
```

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
