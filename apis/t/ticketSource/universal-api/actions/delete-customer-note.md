# TicketSource: Delete Customer Note

Deletes an existing customer note from TicketSource.

```
DELETE https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/delete-customer-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TicketSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/delete-customer-note?connectionId=$CONNECTION_ID&customerId=string&customerNoteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string",
  "customerNoteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/delete-customer-note?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TicketSource API returns.

## Native endpoint

Through the native TicketSource API, this operation is `DELETE /customers/{CustomerId}/notes/{CustomerNoteId}` (base URL `https://api.ticketsource.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer-note.md) for the provider-specific parameters and requirements.

