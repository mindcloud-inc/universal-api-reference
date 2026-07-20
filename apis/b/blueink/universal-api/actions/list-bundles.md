# Blueink: List Bundles

Retrieves bundles from your Blueink account.

```
GET https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-bundles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-bundles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-bundles?${params}`, {
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
| `search` | string | no | Search bundle slug, label, custom key, signer name, email, or phone. |
| `status` | string | no |  |
| `statusIn` | string | no | Comma-separated bundle statuses to include. |
| `tag` | string | no |  |
| `tagIn` | string | no | Comma-separated tags; bundles with any listed tag match. |
| `ordering` | string | no | Sort by created, sent, or completed_at. Prefix with - for descending order. |
| `template` | string | no | Filter bundles created from a specific template ID. |

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

Through the native Blueink API, this operation is `GET /bundles/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bundles.md) for the provider-specific parameters and requirements.

