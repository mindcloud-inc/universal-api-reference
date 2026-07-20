# Anthropic: Create Invite

Creates an invite for the Anthropic organization.

```
POST https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "role": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-invite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "role": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address to invite. |
| `role` | string | yes | Organization role for the invited user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "invitedAt": "2026-05-07T12:00:00.000Z",
      "role": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Invitee email address. |
| `expiresAt` | date | Invite expiration timestamp. |
| `id` | string | Invite ID. |
| `invitedAt` | date | Invite creation timestamp. |
| `role` | string | Invite role. |
| `status` | string | Invite status. |
| `type` | string | Object type. |

## Native endpoint

Through the native Anthropic API, this operation is `POST /v1/organizations/invites` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invite.md) for the provider-specific parameters and requirements.

