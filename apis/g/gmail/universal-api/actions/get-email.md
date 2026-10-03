# Google Mail: Get Email

Retrieves a Gmail message.

```
GET https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-email?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-email?${params}`, {
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
| `id` | list<string> | yes | The immutable ID of the message.. Use the List Emails action to find this value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {
          "attachmentId": "string",
          "contentId": "string",
          "filename": "Ava Chen",
          "inline": true,
          "mimeType": "string",
          "partId": "string",
          "size": 1
        }
      ],
      "date": "string",
      "emailId": "ava@example.com",
      "historyId": "string",
      "htmlContent": "string",
      "labelIds": [
        "string"
      ],
      "messageLink": "https://example.com",
      "originalHeaders": [
        {
          "name": "Ava Chen",
          "value": "string"
        }
      ],
      "simpleHeaders": {
        "recipients": [
          {
            "email": "ava@example.com",
            "name": "Ava Chen"
          }
        ],
        "sender": {
          "email": "ava@example.com",
          "name": "Ava Chen"
        },
        "subject": "string",
        "threadTopic": "string"
      },
      "snippet": "string",
      "subject": "string",
      "textContent": "string",
      "threadId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments[].attachmentId` | string |  |
| `attachments[].contentId` | string |  |
| `attachments[].filename` | string |  |
| `attachments[].inline` | boolean |  |
| `attachments[].mimeType` | string |  |
| `attachments[].partId` | string |  |
| `attachments[].size` | number |  |
| `date` | string |  |
| `emailId` | string |  |
| `historyId` | string |  |
| `htmlContent` | string |  |
| `labelIds[]` | string |  |
| `messageLink` | string |  |
| `originalHeaders[].name` | string |  |
| `originalHeaders[].value` | string |  |
| `simpleHeaders.recipients[].email` | string |  |
| `simpleHeaders.recipients[].name` | string |  |
| `simpleHeaders.sender.email` | string |  |
| `simpleHeaders.sender.name` | string |  |
| `simpleHeaders.subject` | string |  |
| `simpleHeaders.threadTopic` | undefined |  |
| `snippet` | string |  |
| `subject` | string |  |
| `textContent` | string |  |
| `threadId` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `GET /messages/:id` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email.md) for the provider-specific parameters and requirements.

