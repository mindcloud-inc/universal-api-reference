# Ticketbud: Get Ticket By ID

Retrieves a ticket from Ticketbud by ID.

```
GET https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-ticket-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticketbud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-ticket-by-id?connectionId=$CONNECTION_ID&eventId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-ticket-by-id?${params}`, {
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
| `eventId` | string | yes | The Ticketbud event ID that owns the ticket. |
| `id` | string | yes | The Ticketbud ticket ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ticket": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ticket` | object | The requested Ticketbud ticket. |

## Native endpoint

Through the native Ticketbud API, this operation is `GET /events/:eventId/tickets/:id.json` (base URL `https://api.ticketbud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-by-id.md) for the provider-specific parameters and requirements.

