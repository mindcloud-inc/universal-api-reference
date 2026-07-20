# Ticketbud: Get Ticket Sales By Type

Retrieves ticket sales by ticket type from Ticketbud.

```
GET https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-ticket-sales-by-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticketbud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-ticket-sales-by-type?connectionId=$CONNECTION_ID&eventId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketbud/latest/actions/get-ticket-sales-by-type?${params}`, {
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
| `eventId` | string | yes | The Ticketbud event ID that owns the ticket type. |
| `id` | string | yes | The Ticketbud ticket type ID to retrieve sales for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "tickets": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | Ticket-type sales summary metadata. |
| `tickets` | array<object> | Tickets sold for the selected ticket type. |

## Native endpoint

Through the native Ticketbud API, this operation is `GET /events/:eventId/ticket_sales/:id.json` (base URL `https://api.ticketbud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-sales-by-type.md) for the provider-specific parameters and requirements.

