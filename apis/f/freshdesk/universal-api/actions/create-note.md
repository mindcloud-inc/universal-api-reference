# Freshdesk: Create Note

Creates a note on a Freshdesk ticket.

```
POST https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | list<number> | yes | Freshdesk ticket ID. |
| `attachments[]` | array<object> | no | Note attachments |
| `body` | string | no | Note content in HTML |
| `incoming` | boolean | no | Mark note as incoming external activity |
| `notifyEmails[]` | array<string> | no | Emails to notify about this note |
| `private` | boolean | no | Whether the note is private |
| `userId` | list<number> | no | Agent/user ID adding the note |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `structuredBody` | object | no | Structured content body for the note |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "body": "string",
      "bodyText": "string",
      "createdAt": "string",
      "id": 1,
      "incoming": true,
      "private": true,
      "ticketId": 1,
      "toEmails": [
        "ava@example.com"
      ],
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `body` | string |  |
| `bodyText` | string |  |
| `createdAt` | string |  |
| `id` | number |  |
| `incoming` | boolean |  |
| `private` | boolean |  |
| `ticketId` | number |  |
| `toEmails` | array<string> |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Freshdesk API, this operation is `POST /tickets/:ticketId/notes` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

