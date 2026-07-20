# TicketSource: Get Venue

Retrieves a venue from the TicketSource account.

```
GET https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-venue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TicketSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-venue?connectionId=$CONNECTION_ID&venueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "venueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-venue?${params}`, {
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
| `venueId` | string | yes | The unique identifier for a Venue record |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "address": {
          "line1": "string",
          "line2": "string",
          "line3": "string",
          "line4": "string",
          "postcode": "string"
        },
        "boxoffice": {
          "email": "ava@example.com",
          "telephone": "string"
        },
        "createdAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "links": {
        "dates": "https://example.com",
        "event": "https://example.com",
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
| `attributes.address.line1` | string |  |
| `attributes.address.line2` | string |  |
| `attributes.address.line3` | string |  |
| `attributes.address.line4` | string |  |
| `attributes.address.postcode` | string |  |
| `attributes.boxoffice.email` | string |  |
| `attributes.boxoffice.telephone` | string |  |
| `attributes.createdAt` | date |  |
| `attributes.name` | string |  |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `links.dates` | string |  |
| `links.event` | string |  |
| `links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native TicketSource API, this operation is `GET /venues/{VenueId}` (base URL `https://api.ticketsource.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-venue.md) for the provider-specific parameters and requirements.

