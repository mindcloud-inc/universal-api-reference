# Outlook Universal API Examples

These examples use the MindCloud API key and Outlook connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Messages

Retrieves email messages from an Outlook mailbox.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlook/latest/actions/list-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlook/latest/actions/list-messages?${params}`, {
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
      "bccRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "body": {
        "content": "string",
        "contentType": "string"
      },
      "bodyPreview": "string",
      "categories": [
        "string"
      ],
      "ccRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "changeKey": "string",
      "conversationId": "string",
      "conversationIndex": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "flag": {
        "flagStatus": "string"
      },
      "from": {
        "emailAddress": {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      },
      "hasAttachments": true,
      "id": "string",
      "importance": "string",
      "inferenceClassification": "string",
      "internetMessageId": "string",
      "isDeliveryReceiptRequested": true,
      "isDraft": true,
      "isRead": true,
      "isReadReceiptRequested": true,
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "parentFolderId": "string",
      "receivedDateTime": "2026-05-07T12:00:00.000Z",
      "replyTo": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "sender": {
        "emailAddress": {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      },
      "sentDateTime": "2026-05-07T12:00:00.000Z",
      "subject": "string",
      "toRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Messages action reference](actions/list-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/outlook/latest/actions/list-messages).

## Create Draft Message

Creates a draft email in Outlook.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outlook/latest/actions/create-draft-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "Quarterly update",
  "bodyContent": "Write the draft body here.",
  "bodyContentType": "Text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outlook/latest/actions/create-draft-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "Quarterly update",
    "bodyContent": "Write the draft body here.",
    "bodyContentType": "Text"
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
      "bccRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "body": {
        "content": "string",
        "contentType": "string"
      },
      "bodyPreview": "string",
      "categories": [
        "string"
      ],
      "ccRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "changeKey": "string",
      "conversationId": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "flag": {
        "flagStatus": "string"
      },
      "hasAttachments": true,
      "id": "string",
      "importance": "string",
      "internetMessageId": "string",
      "isDraft": true,
      "isRead": true,
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "parentFolderId": "string",
      "receivedDateTime": "2026-05-07T12:00:00.000Z",
      "sentDateTime": "2026-05-07T12:00:00.000Z",
      "subject": "string",
      "toRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Draft Message action reference](actions/create-draft-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/outlook/latest/actions/create-draft-message).
