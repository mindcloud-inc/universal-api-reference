# SuperOps IT: List Ticket Notes



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-ticket-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-ticket-notes?connectionId=$CONNECTION_ID&ticketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-ticket-notes?${params}`, {
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
| `ticketId` | string | yes | The SuperOps ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "getTicketNoteList": [
        {
          "addedBy": {
            "name": "Ava Chen",
            "userId": "string"
          },
          "addedOn": "2026-05-07T12:00:00.000Z",
          "content": "string",
          "noteId": "string",
          "privacyType": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `getTicketNoteList[].addedBy.name` | string |  |
| `getTicketNoteList[].addedBy.userId` | string |  |
| `getTicketNoteList[].addedOn` | date |  |
| `getTicketNoteList[].content` | string |  |
| `getTicketNoteList[].noteId` | string |  |
| `getTicketNoteList[].privacyType` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-notes.md) for the provider-specific parameters and requirements.

