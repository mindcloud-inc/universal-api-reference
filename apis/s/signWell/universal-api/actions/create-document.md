# SignWell: Create Document

Creates a new document in SignWell.

```
POST https://connect.mindcloud.co/v1/universal/signWell/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files[]": [
    {}
  ],
  "files[].file_url": "https://example.com",
  "recipients[]": [
    {}
  ],
  "recipients[].id": "string",
  "recipients[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signWell/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files[]": [{}],
    "files[].file_url": "https://example.com",
    "recipients[]": [{}],
    "recipients[].id": "string",
    "recipients[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `test_mode` | boolean | no |  |
| `draft` | boolean | no |  |
| `files[]` | array<object> | yes |  |
| `files[].name` | string | no |  |
| `files[].file_url` | string | yes |  |
| `recipients[]` | array<object> | yes |  |
| `recipients[].id` | string | yes |  |
| `recipients[].email` | string | yes |  |
| `recipients[].name` | string | no |  |
| `recipients[].placeholder_name` | string | no |  |

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
      "embeddedEditUrl": "https://example.com",
      "embeddedPreviewUrl": {},
      "embeddedSigning": true,
      "errorMessage": {},
      "expiresIn": 1,
      "files": [
        {
          "name": "Ava Chen",
          "pagesNumber": 1
        }
      ],
      "id": "string",
      "language": "string",
      "message": {},
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
      "subject": {},
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
| `embeddedEditUrl` | string |  |
| `embeddedPreviewUrl` | object |  |
| `embeddedSigning` | boolean |  |
| `errorMessage` | object |  |
| `expiresIn` | number |  |
| `files[].name` | string |  |
| `files[].pagesNumber` | number |  |
| `id` | string |  |
| `language` | string |  |
| `message` | object |  |
| `name` | string |  |
| `recipients[].bounced` | object |  |
| `recipients[].bouncedDetails` | object |  |
| `recipients[].email` | string |  |
| `recipients[].id` | string |  |
| `recipients[].message` | object |  |
| `recipients[].name` | string |  |
| `recipients[].passcode` | object |  |
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
| `subject` | object |  |
| `testMode` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native SignWell API, this operation is `POST /documents` (base URL `https://www.signwell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

