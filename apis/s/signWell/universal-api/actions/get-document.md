# SignWell: Get Document

Retrieves document details and recipients from SignWell.

```
GET https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-document?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-document?${params}`, {
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

Through the native SignWell API, this operation is `GET /documents/:id` (base URL `https://www.signwell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

