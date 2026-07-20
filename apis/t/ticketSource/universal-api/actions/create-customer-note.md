# TicketSource: Create Customer Note

Creates a new customer note in TicketSource.

```
POST https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/create-customer-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TicketSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/create-customer-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/create-customer-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | The unique identifier for a Customer record |
| `data` | object | no | A Customer Note against a specific Customer record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "createdBy": "string",
        "description": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "links": {
        "customer": "https://example.com",
        "self": "https://example.com"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | date |  |
| `attributes.createdBy` | string |  |
| `attributes.description` | string |  |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `links.customer` | string |  |
| `links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native TicketSource API, this operation is `POST /customers/{CustomerId}/notes` (base URL `https://api.ticketsource.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-note.md) for the provider-specific parameters and requirements.

