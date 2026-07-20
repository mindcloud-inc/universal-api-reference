# PostHog: Add or Invite Members

Creates an organization invite in PostHog.

```
POST https://connect.mindcloud.co/v1/universal/postHog/latest/actions/add-or-invite-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostHog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postHog/latest/actions/add-or-invite-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "0196354e-4380-0000-cc07-8aa6be2ca63f",
  "targetEmail": "teammate@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postHog/latest/actions/add-or-invite-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "0196354e-4380-0000-cc07-8aa6be2ca63f",
    "targetEmail": "teammate@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | UUID of the organization. Example: `0196354e-4380-0000-cc07-8aa6be2ca63f`. |
| `targetEmail` | string | yes | Email address to invite. Example: `teammate@example.com`. |
| `firstName` | string | no | First name of the invited user. Example: `Alex`. |
| `level` | list<number> | no | Organization membership level (1 member, 8 administrator, 15 owner). One of: `1`, `15`, `8`. |
| `message` | string | no | Optional invitation message. Example: `Welcome to our PostHog workspace.`. |
| `sendEmail` | boolean | no | Whether to send the invite email. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `private_project_access[]` | array<object> | no | List of private project access entries (team/project IDs with access levels). |
| `combinePendingInvites` | boolean | no | Whether to combine with existing pending invites for the same email. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "emailingAttemptMade": true,
      "firstName": "Ava",
      "id": "string",
      "isExpired": true,
      "level": 1,
      "message": "string",
      "privateProjectAccess": [
        {}
      ],
      "targetEmail": "ava@example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Invite creation timestamp. |
| `createdBy` | object | User who created the invite. |
| `emailingAttemptMade` | boolean | Whether email delivery was attempted. |
| `firstName` | string | First name sent with invite. |
| `id` | string | Organization invite UUID. |
| `isExpired` | boolean | Whether invite has expired. |
| `level` | number | Organization membership level. |
| `message` | string | Optional invite message. |
| `privateProjectAccess` | array<object> | Private project access mapping attached to invite. |
| `targetEmail` | string | Email being invited. |
| `updatedAt` | date | Invite update timestamp. |

## Native endpoint

Through the native PostHog API, this operation is `POST /organizations/:organizationId/invites/` (base URL `https://us.posthog.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-or-invite-members.md) for the provider-specific parameters and requirements.

