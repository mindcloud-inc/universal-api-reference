# Blueink Universal API Examples

These examples use the MindCloud API key and Blueink connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bundles

Retrieves bundles from your Blueink account.

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

Example response:

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

See the full [List Bundles action reference](actions/list-bundles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blueink/latest/actions/list-bundles).

## Add Bundle Tags

Adds tags to a Blueink bundle.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/add-bundle-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bundleSlug": "string",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueink/latest/actions/add-bundle-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bundleSlug": "string",
    "tags[]": ["string"]
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Add Bundle Tags action reference](actions/add-bundle-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blueink/latest/actions/add-bundle-tags).
