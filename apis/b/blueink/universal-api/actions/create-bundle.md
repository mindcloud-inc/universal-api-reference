# Blueink: Create Bundle

Creates a new bundle in Blueink.

```
POST https://connect.mindcloud.co/v1/universal/blueink/latest/actions/create-bundle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/create-bundle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packets[].key": "string",
  "packets[].name": "Ava Chen",
  "packets[].email": "ava@example.com",
  "documents[].template_id": "string",
  "documents[].assignments[].role": "string",
  "documents[].assignments[].signer": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueink/latest/actions/create-bundle', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packets[].key": "string",
    "packets[].name": "Ava Chen",
    "packets[].email": "ava@example.com",
    "documents[].template_id": "string",
    "documents[].assignments[].role": "string",
    "documents[].assignments[].signer": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isTest` | boolean | no | Create the bundle as a test bundle. |
| `status` | string | no | Use dr to create a draft bundle without sending it. |
| `packets[].key` | string | yes | Unique signer key for the bundle. |
| `packets[].name` | string | yes | Name of the signer. |
| `packets[].email` | string | yes | Email address of the signer. |
| `documents[].template_id` | string | yes | Document template ID to include in the bundle. |
| `documents[].assignments[].role` | string | yes | Template role to assign. |
| `documents[].assignments[].signer` | string | yes | Signer key to bind to the template role. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ccSender": true,
      "completedAt": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "customKey": "string",
      "customText": "string",
      "documents": [
        {
          "key": "string",
          "name": "Ava Chen",
          "order": 1,
          "templateId": "string"
        }
      ],
      "emailFooter": "ava@example.com",
      "emailMessage": "ava@example.com",
      "emailSubject": "ava@example.com",
      "expires": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "inOrder": true,
      "isTest": true,
      "label": "string",
      "packets": [
        {
          "authId": true,
          "authSelfie": true,
          "authSms": true,
          "completedAt": "2026-05-07T12:00:00.000Z",
          "deliverVia": "string",
          "email": "ava@example.com",
          "id": "string",
          "key": "string",
          "lastAccessedAt": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "order": 1,
          "personId": "string",
          "phone": "string",
          "signingCompleteRedirect": "string",
          "status": "string",
          "suppressAll": true,
          "suppressDocsReady": true,
          "suppressReminder": true,
          "suppressSigning": true
        }
      ],
      "reminderExpires": 1,
      "reminderInterval": 1,
      "reminderOffset": 1,
      "requesterEmail": "ava@example.com",
      "requesterName": "Ava Chen",
      "sendReminders": true,
      "sent": "2026-05-07T12:00:00.000Z",
      "smsMessage": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ccSender` | boolean |  |
| `completedAt` | date |  |
| `created` | date |  |
| `customKey` | string |  |
| `customText` | string |  |
| `documents[].key` | string |  |
| `documents[].name` | string |  |
| `documents[].order` | number |  |
| `documents[].templateId` | string |  |
| `emailFooter` | string |  |
| `emailMessage` | string |  |
| `emailSubject` | string |  |
| `expires` | date |  |
| `id` | string |  |
| `inOrder` | boolean |  |
| `isTest` | boolean |  |
| `label` | string |  |
| `packets[].authId` | boolean |  |
| `packets[].authSelfie` | boolean |  |
| `packets[].authSms` | boolean |  |
| `packets[].completedAt` | date |  |
| `packets[].deliverVia` | string |  |
| `packets[].email` | string |  |
| `packets[].id` | string |  |
| `packets[].key` | string |  |
| `packets[].lastAccessedAt` | date |  |
| `packets[].name` | string |  |
| `packets[].order` | number |  |
| `packets[].personId` | string |  |
| `packets[].phone` | string |  |
| `packets[].signingCompleteRedirect` | string |  |
| `packets[].status` | string |  |
| `packets[].suppressAll` | boolean |  |
| `packets[].suppressDocsReady` | boolean |  |
| `packets[].suppressReminder` | boolean |  |
| `packets[].suppressSigning` | boolean |  |
| `reminderExpires` | number |  |
| `reminderInterval` | number |  |
| `reminderOffset` | number |  |
| `requesterEmail` | string |  |
| `requesterName` | string |  |
| `sendReminders` | boolean |  |
| `sent` | date |  |
| `smsMessage` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Blueink API, this operation is `POST /bundles/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bundle.md) for the provider-specific parameters and requirements.

