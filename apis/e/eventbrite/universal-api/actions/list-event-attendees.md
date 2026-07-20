# Eventbrite: List Event Attendees

Retrieves event attendees from Eventbrite.

```
GET https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-event-attendees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-event-attendees?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-event-attendees?${params}`, {
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
| `eventId` | string | yes | Event identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate": {},
      "barcodes": [
        {
          "barcode": "string",
          "changed": "string",
          "checkinType": 1,
          "created": "string",
          "isPrinted": true,
          "status": "string"
        }
      ],
      "cancelled": true,
      "changed": "string",
      "checkedIn": true,
      "costs": {
        "basePrice": {
          "currency": "string",
          "display": "string",
          "majorValue": "string",
          "value": 1
        },
        "eventbriteFee": {
          "currency": "string",
          "display": "string",
          "majorValue": "string",
          "value": 1
        },
        "gross": {
          "currency": "string",
          "display": "string",
          "majorValue": "string",
          "value": 1
        },
        "paymentFee": {
          "currency": "string",
          "display": "string",
          "majorValue": "string",
          "value": 1
        },
        "tax": {
          "currency": "string",
          "display": "string",
          "majorValue": "string",
          "value": 1
        }
      },
      "created": "string",
      "deliveryMethod": "string",
      "eventId": "string",
      "guestlistId": {},
      "id": "string",
      "invitedBy": {},
      "orderId": "string",
      "profile": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen"
      },
      "quantity": 1,
      "refunded": true,
      "resourceUri": "string",
      "status": "string",
      "ticketClassId": "string",
      "ticketClassName": "Ava Chen",
      "variantId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate` | object |  |
| `barcodes[].barcode` | string |  |
| `barcodes[].changed` | string |  |
| `barcodes[].checkinType` | number |  |
| `barcodes[].created` | string |  |
| `barcodes[].isPrinted` | boolean |  |
| `barcodes[].status` | string |  |
| `cancelled` | boolean |  |
| `changed` | string |  |
| `checkedIn` | boolean |  |
| `costs.basePrice.currency` | string |  |
| `costs.basePrice.display` | string |  |
| `costs.basePrice.majorValue` | string |  |
| `costs.basePrice.value` | number |  |
| `costs.eventbriteFee.currency` | string |  |
| `costs.eventbriteFee.display` | string |  |
| `costs.eventbriteFee.majorValue` | string |  |
| `costs.eventbriteFee.value` | number |  |
| `costs.gross.currency` | string |  |
| `costs.gross.display` | string |  |
| `costs.gross.majorValue` | string |  |
| `costs.gross.value` | number |  |
| `costs.paymentFee.currency` | string |  |
| `costs.paymentFee.display` | string |  |
| `costs.paymentFee.majorValue` | string |  |
| `costs.paymentFee.value` | number |  |
| `costs.tax.currency` | string |  |
| `costs.tax.display` | string |  |
| `costs.tax.majorValue` | string |  |
| `costs.tax.value` | number |  |
| `created` | string |  |
| `deliveryMethod` | string |  |
| `eventId` | string |  |
| `guestlistId` | object |  |
| `id` | string |  |
| `invitedBy` | object |  |
| `orderId` | string |  |
| `profile.email` | string |  |
| `profile.firstName` | string |  |
| `profile.lastName` | string |  |
| `profile.name` | string |  |
| `quantity` | number |  |
| `refunded` | boolean |  |
| `resourceUri` | string |  |
| `status` | string |  |
| `ticketClassId` | string |  |
| `ticketClassName` | string |  |
| `variantId` | object |  |

## Native endpoint

Through the native Eventbrite API, this operation is `GET /events/:eventId/attendees/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-attendees.md) for the provider-specific parameters and requirements.

