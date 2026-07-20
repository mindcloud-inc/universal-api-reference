# TicketSource: Get Customer Note

Retrieves a customer note from TicketSource.

```
GET https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-customer-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TicketSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-customer-note?connectionId=$CONNECTION_ID&customerId=string&customerNoteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string",
  "customerNoteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-customer-note?${params}`, {
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
| `customerId` | string | yes | The unique identifier for a Customer record |
| `customerNoteId` | string | yes | The unique identifier for a Customer Note record |

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

Through the native TicketSource API, this operation is `GET /customers/{CustomerId}/notes/{CustomerNoteId}` (base URL `https://api.ticketsource.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-note.md) for the provider-specific parameters and requirements.

