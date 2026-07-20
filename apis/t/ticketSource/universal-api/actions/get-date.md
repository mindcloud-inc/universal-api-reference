# TicketSource: Get Date

Retrieves an event date from TicketSource.

```
GET https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TicketSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-date?connectionId=$CONNECTION_ID&dateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-date?${params}`, {
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
| `dateId` | string | yes | The unique identifier for a Date record |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "cancelled": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "doorsOpen": "string",
        "end": "string",
        "onSale": true,
        "onSaleEnd": "string",
        "onSaleStart": "string",
        "public": true,
        "start": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "links": {
        "bookings": "https://example.com",
        "bookNow": "https://example.com",
        "event": "https://example.com",
        "self": "https://example.com",
        "venue": "https://example.com"
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
| `attributes.cancelled` | boolean |  |
| `attributes.createdAt` | date |  |
| `attributes.doorsOpen` | string |  |
| `attributes.end` | string |  |
| `attributes.onSale` | boolean |  |
| `attributes.onSaleEnd` | string |  |
| `attributes.onSaleStart` | string |  |
| `attributes.public` | boolean |  |
| `attributes.start` | string |  |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `links.bookings` | string |  |
| `links.bookNow` | string |  |
| `links.event` | string |  |
| `links.self` | string |  |
| `links.venue` | string |  |
| `type` | string |  |

## Native endpoint

Through the native TicketSource API, this operation is `GET /dates/{DateId}` (base URL `https://api.ticketsource.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-date.md) for the provider-specific parameters and requirements.

