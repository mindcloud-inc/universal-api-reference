# SuperOps IT: Create Ticket Note



```
POST https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-ticket-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-ticket-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-ticket-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | The SuperOps ticket ID. |
| `content` | string | yes | The note content. |
| `addedByUserId` | string | no | Optional technician user ID adding the note. |
| `addedOn` | date | no | Optional note creation time in ISO 8601 format. |
| `privacyType` | string | no | PUBLIC or PRIVATE. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTicketNote": {
        "addedBy": {
          "name": "Ava Chen",
          "userId": "string"
        },
        "addedOn": "2026-05-07T12:00:00.000Z",
        "content": "string",
        "noteId": "string",
        "privacyType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTicketNote.addedBy.name` | string |  |
| `createTicketNote.addedBy.userId` | string |  |
| `createTicketNote.addedOn` | date |  |
| `createTicketNote.content` | string |  |
| `createTicketNote.noteId` | string |  |
| `createTicketNote.privacyType` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket-note.md) for the provider-specific parameters and requirements.

