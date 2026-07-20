# Moxie: Create Ticket

Creates a new ticket in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userEmail": "ava@example.com",
  "ticketType": "string",
  "subject": "string",
  "comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userEmail": "ava@example.com",
    "ticketType": "string",
    "subject": "string",
    "comment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userEmail` | string | yes | Email of the user creating the ticket. |
| `ticketType` | string | yes | Ticket type identifier. |
| `subject` | string | yes | Ticket subject line. |
| `comment` | string | yes | Initial ticket comment body. |
| `dueDate` | date | no | Ticket due date. |
| `formData` | object | no | Ticket form data object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "ticket": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> |  |
| `ticket` | object |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/tickets/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

