# CINCEL: Get Document Invite



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-document-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-document-invite?connectionId=$CONNECTION_ID&team=string&folder=string&document=string&invite=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team": "string",
  "folder": "string",
  "document": "string",
  "invite": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-document-invite?${params}`, {
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
| `team` | string | yes | Team UUID from the path. |
| `folder` | string | yes | Folder UUID from the path. |
| `document` | string | yes | Document UUID from the path. |
| `invite` | string | yes | Invite UUID from the path. |

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
| `createdAt` | date | Invite creation timestamp. |
| `deletedAt` | date | Invite deletion timestamp when present. |
| `document` | string | Document UUID. |
| `email` | string | Invitee email address. |
| `expectedRfc` | string | Expected RFC when configured. |
| `identityVerification` | boolean | Whether identity verification is required. |
| `identityVerificationAttemptsLimit` | number | Maximum identity verification attempts when configured. |
| `name` | string | Invitee name. |
| `reminderFrequency` | number | Reminder frequency when configured. |
| `rfcValidated` | boolean | Whether RFC has been validated. |
| `rfcValidation` | boolean | Whether RFC validation is required. |
| `sentAt` | date | Invite sent timestamp when present. |
| `signatureAllowedTypes` | string | Allowed signature types. |
| `signatureCoordinates` | array<object> | Explicit signature coordinates when configured. |
| `signatureNotifyCreator` | boolean | Whether creator is notified on signature. |
| `signatureType` | string | Selected signature type when present. |
| `stage` | number | Invite stage. |
| `status` | string | Invite status. |
| `type` | string | Invite role. |
| `updatedAt` | date | Invite update timestamp. |
| `userCoordinates` | boolean | Whether geolocation is required. |
| `uuid` | string | Invite UUID. |

## Native endpoint

Through the native CINCEL API, this operation is `GET /teams/:team/folders/:folder/documents/:document/invites/:invite` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-invite.md) for the provider-specific parameters and requirements.

