# CINCEL: Update Document Invite



```
PUT https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/update-document-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/update-document-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "team": "string",
  "folder": "string",
  "document": "string",
  "invite": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/update-document-invite', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "team": "string",
    "folder": "string",
    "document": "string",
    "invite": "string"
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
| `invite` | string | yes | Invite UUID from the path. |
| `name` | string | no | Updated invite recipient name. |
| `email` | string | no | Updated invite recipient email. |
| `reminderFrequency` | number | no | Optional reminder interval value for the invite. |

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
      "signatureAllowedTypes": "string",
      "signatureCoordinates": [
        {}
      ],
      "signatureNotifyCreator": true,
      "signatureType": "string",
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
| `createdAt` | date | Creation timestamp. |
| `deletedAt` | date | When the invite was deleted. |
| `document` | string | Document UUID. |
| `email` | string | Invitee email address. |
| `expectedRfc` | string | Expected RFC value when validation is enabled. |
| `identityVerification` | boolean | Whether identity verification is enabled. |
| `identityVerificationAttemptsLimit` | number | Maximum identity verification attempts. |
| `name` | string | Invitee name. |
| `reminderFrequency` | number | Reminder frequency value. |
| `rfcValidated` | boolean | Whether the RFC has already been validated. |
| `rfcValidation` | boolean | Whether RFC validation is enabled. |
| `sentAt` | date | When the invite was sent. |
| `signatureAllowedTypes` | string | Allowed signature type set. |
| `signatureCoordinates` | array<object> | Explicit signature placement coordinates. |
| `signatureNotifyCreator` | boolean | Whether the creator is notified after signature. |
| `signatureType` | string | Default signature type. |
| `stage` | number | Invite stage. |
| `status` | string | Invite status. |
| `type` | string | Invite type. |
| `updatedAt` | date | Last update timestamp. |
| `userCoordinates` | boolean | Whether user-provided signature coordinates are enabled. |
| `uuid` | string | Invite UUID. |

## Native endpoint

Through the native CINCEL API, this operation is `PATCH /teams/:team/folders/:folder/documents/:document/invites/:invite` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document-invite.md) for the provider-specific parameters and requirements.

