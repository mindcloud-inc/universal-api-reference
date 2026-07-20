# ManyReach: List Messages

Retrieves messages from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-messages?connectionId=$CONNECTION_ID&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-messages?${params}`, {
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
| `type` | string | yes | Message type filter. Valid values: Sent, Reply, SentManual. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "campaignId": 1,
      "clickCount": 1,
      "clickDetails": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "followupId": 1,
      "fromEmail": "ava@example.com",
      "messageId": "string",
      "openCount": 1,
      "subject": "string",
      "toEmail": "ava@example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string | The body content of the email message. HTML content should be handled or sanitized appropriately on the client side. |
| `campaignId` | number | ID of the campaign this message is associated with, if applicable. |
| `clickCount` | number | Number of times links in this message were clicked. Only applicable to SENT messages. |
| `clickDetails` | array<object> | Detailed click tracking information for links in the message. Only applicable to SENT messages. |
| `createdAt` | date | Timestamp when the message was created or sent. |
| `followupId` | number | Followup ID (FUID) associated with this message, if applicable. |
| `fromEmail` | string | Email address of the sender. |
| `messageId` | string | Unique identifier for the message, using either SentID or ReplyID depending on the message type. |
| `openCount` | number | Number of times this message was opened. Only applicable to SENT messages. |
| `subject` | string | Email subject line. |
| `toEmail` | string | Email address of the recipient. |
| `type` | string | Message type indicating whether this is a sent message or a reply. Valid values: SENT or REPLY. |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/messages` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

