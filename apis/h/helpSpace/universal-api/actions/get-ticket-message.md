# HelpSpace: Get Ticket Message

Retrieves a ticket message from HelpSpace.

```
GET https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-ticket-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-ticket-message?connectionId=$CONNECTION_ID&messageId=string&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string",
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-ticket-message?${params}`, {
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
| `messageId` | string | yes | HelpSpace message identifier. |
| `ticketId` | string | yes | HelpSpace ticket identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "bcc": [
        "string"
      ],
      "body": "string",
      "cc": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fromContact": {},
      "id": 1,
      "inlineImages": [
        {}
      ],
      "subject": "string",
      "to": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `bcc` | array<string> |  |
| `body` | string |  |
| `cc` | array<string> |  |
| `createdAt` | date |  |
| `fromContact` | object |  |
| `id` | number |  |
| `inlineImages` | array<object> |  |
| `subject` | string |  |
| `to` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native HelpSpace API, this operation is `GET /tickets/{ticket_id}/messages/{message_id}` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-message.md) for the provider-specific parameters and requirements.

