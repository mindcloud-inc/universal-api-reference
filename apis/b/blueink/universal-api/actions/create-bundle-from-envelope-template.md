# Blueink: Create Bundle from Envelope Template

Creates a Blueink bundle from an envelope template.

```
POST https://connect.mindcloud.co/v1/universal/blueink/latest/actions/create-bundle-from-envelope-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/create-bundle-from-envelope-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "envelope_template.template_id": "string",
  "packets[].key": "string",
  "packets[].name": "Ava Chen",
  "packets[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueink/latest/actions/create-bundle-from-envelope-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "envelope_template.template_id": "string",
    "packets[].key": "string",
    "packets[].name": "Ava Chen",
    "packets[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | no | A label to help you identify this Bundle |
| `isTest` | boolean | no | Set to true while the integration is under development |
| `status` | string | no | Leave blank to send normally or use dr to create a draft bundle |
| `envelope_template.template_id` | string | yes | The envelope template identifier to instantiate |
| `packets[].key` | string | yes | The signer role key from the envelope template |
| `packets[].name` | string | yes | The recipient name for this packet |
| `packets[].email` | string | yes | The recipient email address for this packet |
| `packets[].phone` | string | no | The recipient phone number for this packet when SMS delivery or SMS auth is used |
| `packets[].deliver_via` | string | no | How Blueink should deliver the signing request |

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

Through the native Blueink API, this operation is `POST /bundles/create_from_envelope_template/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bundle-from-envelope-template.md) for the provider-specific parameters and requirements.

