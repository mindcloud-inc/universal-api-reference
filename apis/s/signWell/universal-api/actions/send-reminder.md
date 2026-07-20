# SignWell: Send Reminder

Sends a reminder for an unsigned document in SignWell.

```
POST https://connect.mindcloud.co/v1/universal/signWell/latest/actions/send-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/send-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signWell/latest/actions/send-reminder', {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowDecline": true,
      "allowReassign": true,
      "apiApplicationId": {},
      "applySigningOrder": true,
      "archived": true,
      "createdAt": "string",
      "customRequesterEmail": {},
      "customRequesterName": {},
      "declineMessage": {},
      "declineRedirectUrl": {},
      "embeddedEditUrl": {},
      "embeddedPreviewUrl": "https://example.com",
      "embeddedSigning": true,
      "errorMessage": {},
      "expiresIn": 1,
      "fields": [
        {}
      ],
      "files": [
        {
          "name": "Ava Chen",
          "pagesNumber": 1
        }
      ],
      "id": "string",
      "language": "string",
      "message": "string",
      "name": "Ava Chen",
      "recipients": [
        {
          "bounced": {},
          "bouncedDetails": {},
          "email": "ava@example.com",
          "id": "string",
          "message": {},
          "name": "Ava Chen",
          "passcode": {},
          "placeholderName": "Ava Chen",
          "sendEmail": true,
          "sendEmailDelay": 1,
          "signingOrder": 1,
          "signingUrl": "https://example.com",
          "status": "string",
          "subject": {}
        }
      ],
      "redirectUrl": {},
      "reminders": true,
      "requesterEmailAddress": "ava@example.com",
      "status": "string",
      "subject": "string",
      "templateId": "string",
      "testMode": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowDecline` | boolean |  |
| `allowReassign` | boolean |  |
| `apiApplicationId` | object |  |
| `applySigningOrder` | boolean |  |
| `archived` | boolean |  |
| `createdAt` | string |  |
| `customRequesterEmail` | object |  |
| `customRequesterName` | object |  |
| `declineMessage` | object |  |
| `declineRedirectUrl` | object |  |
| `embeddedEditUrl` | object |  |
| `embeddedPreviewUrl` | string |  |
| `embeddedSigning` | boolean |  |
| `errorMessage` | object |  |
| `expiresIn` | number |  |
| `fields[]` | object |  |
| `files[].name` | string |  |
| `files[].pagesNumber` | number |  |
| `id` | string |  |
| `language` | string |  |
| `message` | string |  |
| `name` | string |  |
| `recipients[].bounced` | object |  |
| `recipients[].bouncedDetails` | object |  |
| `recipients[].email` | string |  |
| `recipients[].id` | string |  |
| `recipients[].message` | object |  |
| `recipients[].name` | string |  |
| `recipients[].passcode` | object |  |
| `recipients[].placeholderName` | string |  |
| `recipients[].sendEmail` | boolean |  |
| `recipients[].sendEmailDelay` | number |  |
| `recipients[].signingOrder` | number |  |
| `recipients[].signingUrl` | string |  |
| `recipients[].status` | string |  |
| `recipients[].subject` | object |  |
| `redirectUrl` | object |  |
| `reminders` | boolean |  |
| `requesterEmailAddress` | string |  |
| `status` | string |  |
| `subject` | string |  |
| `templateId` | string |  |
| `testMode` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native SignWell API, this operation is `POST /documents/:id/remind` (base URL `https://www.signwell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-reminder.md) for the provider-specific parameters and requirements.

