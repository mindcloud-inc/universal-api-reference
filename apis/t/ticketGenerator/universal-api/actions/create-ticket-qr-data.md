# Ticket Generator: Create Ticket QR Data

Creates ticket QR code data and ticket ID in Ticket Generator.

```
POST https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/create-ticket-qr-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Generator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/create-ticket-qr-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string",
  "width": "300"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/create-ticket-qr-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string",
    "width": "300"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | Ticket Generator event identifier. |
| `ticketCategoryId` | string | no | Ticket category identifier. Optional when the event has exactly one ticket category. |
| `width` | number | yes | Generated ticket width in pixels. Default: `300`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base64EncodedUrl": "https://example.com",
      "ticketCategoryName": "Ava Chen",
      "ticketId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base64EncodedUrl` | string |  |
| `ticketCategoryName` | string |  |
| `ticketId` | number |  |

## Native endpoint

Through the native Ticket Generator API, this operation is `POST v1/ticket/data/` (base URL `https://apis.ticket-generator.com/client`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket-qr-data.md) for the provider-specific parameters and requirements.

