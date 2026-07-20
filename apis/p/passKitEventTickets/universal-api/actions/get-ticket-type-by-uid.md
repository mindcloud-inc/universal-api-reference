# PassKit Event Tickets: Get Ticket Type By Uid

Retrieves a ticket type by user-defined ID from PassKit.

```
GET https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-ticket-type-by-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Event Tickets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-ticket-type-by-uid?connectionId=$CONNECTION_ID&productionId=string&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productionId": "string",
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-ticket-type-by-uid?${params}`, {
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
| `productionId` | string | yes | PassKit production id for the ticket type lookup. |
| `uid` | string | yes | Provider uid for the ticket type lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "ticketTypeId": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `ticketTypeId` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native PassKit Event Tickets API, this operation is `GET /eventTickets/ticketType/uid/:productionId/:uid` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-type-by-uid.md) for the provider-specific parameters and requirements.

