# CINCEL: Create Document Invite



```
POST https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/create-document-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/create-document-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "team": "string",
  "folder": "string",
  "document": "string",
  "name": "Ava Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/create-document-invite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "team": "string",
    "folder": "string",
    "document": "string",
    "name": "Ava Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `team` | string | yes | Team UUID from the path. |
| `folder` | string | yes | Folder UUID from the path. |
| `document` | string | yes | Document UUID from the path. |
| `name` | string | yes | Invitee name. |
| `email` | string | yes | Invitee email address. |
| `reminderFrequency` | number | no | Reminder frequency for the invite. |
| `type` | string | no | Invite role for the recipient. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "document": "string",
      "email": "ava@example.com",
      "expectedRfc": "string",
      "identityVerification": true,
      "identityVerificationAttemptsLimit": 1,
      "name": "Ava Chen",
      "reminderFrequency": 1,
      "rfcValidated": true,
      "rfcValidation": true,
      "sentAt": "2026-05-07T12:00:00.000Z",
      "stage": 1,
      "status": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userCoordinates": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Invite creation timestamp. |
| `deletedAt` | date | Invite deletion timestamp when present. |
| `document` | string | Document UUID. |
| `email` | string | Invitee email address. |
| `expectedRfc` | string | Expected RFC value when configured. |
| `identityVerification` | boolean | Whether identity verification is required. |
| `identityVerificationAttemptsLimit` | number | Maximum identity verification attempts when configured. |
| `name` | string | Invitee name. |
| `reminderFrequency` | number | Reminder frequency when configured. |
| `rfcValidated` | boolean | Whether RFC has been validated. |
| `rfcValidation` | boolean | Whether RFC validation is required. |
| `sentAt` | date | Invite sent timestamp when present. |
| `stage` | number | Invite stage. |
| `status` | string | Invite status. |
| `type` | string | Invite role. |
| `updatedAt` | date | Invite update timestamp. |
| `userCoordinates` | boolean | Whether geolocation is required. |
| `uuid` | string | Invite UUID. |

## Native endpoint

Through the native CINCEL API, this operation is `POST /teams/:team/folders/:folder/documents/:document/invites` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-invite.md) for the provider-specific parameters and requirements.

