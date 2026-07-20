# GrooveHQ: Get Ticket

Retrieves a ticket from GrooveHQ.

```
GET https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrooveHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-ticket?connectionId=$CONNECTION_ID&ticketNumber=1001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketNumber": "1001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-ticket?${params}`, {
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
| `ticketNumber` | string | yes | Example: `1001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastMessageAuthor": {},
      "links": {},
      "mailbox": "string",
      "mailboxId": "string",
      "messageCount": 1,
      "number": 1,
      "state": "string",
      "summary": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Ticket creation timestamp. |
| `id` | number | Internal ticket ID. |
| `lastMessageAuthor` | object | Latest message author summary. |
| `links` | object | Provider links for related resources. |
| `mailbox` | string | Mailbox display name. |
| `mailboxId` | string | Mailbox identifier. |
| `messageCount` | number | Message count on the ticket. |
| `number` | number | Ticket number shown in Groove. |
| `state` | string | Current ticket state. |
| `summary` | string | Latest ticket summary text. |
| `tags` | array<string> | Applied ticket tags. |
| `updatedAt` | date | Latest ticket update timestamp. |

## Native endpoint

Through the native GrooveHQ API, this operation is `GET /tickets/:ticketNumber` (base URL `https://api.groovehq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket.md) for the provider-specific parameters and requirements.

