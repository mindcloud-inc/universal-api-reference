# Microsoft 365 Outlook Universal API Examples

These examples use the MindCloud API key and Microsoft 365 Outlook connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Inbox Messages

Retrieves inbox messages from Microsoft 365 Outlook.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/list-inbox-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/list-inbox-messages?${params}`, {
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
      "bodyPreview": "string",
      "from": {
        "emailAddress": {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      },
      "hasAttachments": true,
      "id": "string",
      "importance": "string",
      "isRead": true,
      "receivedDateTime": "2026-05-07T12:00:00.000Z",
      "sentDateTime": "2026-05-07T12:00:00.000Z",
      "subject": "string",
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Inbox Messages action reference](actions/list-inbox-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoft365Outlook/latest/actions/list-inbox-messages).

## Add File Attachment to Message

Adds a file attachment to a message in Microsoft 365 Outlook.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/add-file-attachment-to-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string",
  "name": "Ava Chen",
  "contentType": "text/plain",
  "contentBytes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/add-file-attachment-to-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string",
    "name": "Ava Chen",
    "contentType": "text/plain",
    "contentBytes": "string"
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
      "@odata": {
        "type": "string"
      },
      "contentBytes": "string",
      "contentType": "string",
      "id": "string",
      "isInline": true,
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

See the full [Add File Attachment to Message action reference](actions/add-file-attachment-to-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoft365Outlook/latest/actions/add-file-attachment-to-message).
