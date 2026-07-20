# Eventbrite: Create Event Ticket Class

Creates a new event ticket class in Eventbrite.

```
POST https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-event-ticket-class
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-event-ticket-class" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string",
  "ticketClass.free": true,
  "ticketClass.name": "Ava Chen",
  "ticketClass.quantityTotal": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-event-ticket-class', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string",
    "ticketClass.free": true,
    "ticketClass.name": "Ava Chen",
    "ticketClass.quantityTotal": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | Event identifier. |
| `ticketClass.free` | boolean | yes | Whether this ticket class is free. |
| `ticketClass.name` | string | yes | Ticket class display name. |
| `ticketClass.quantityTotal` | number | yes | Total quantity for this ticket class. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualCost": {},
      "actualFee": {},
      "autoHide": true,
      "capacity": 1,
      "category": "string",
      "cost": {},
      "deliveryMethods": [
        "string"
      ],
      "description": {},
      "displayName": "Ava Chen",
      "donation": true,
      "eventId": "string",
      "fee": {},
      "free": true,
      "hasPdfTicket": true,
      "hidden": true,
      "hiddenCurrently": true,
      "hideDescription": true,
      "hideSaleDates": true,
      "id": "string",
      "imageId": {},
      "includeFee": true,
      "maximumQuantity": {},
      "maximumQuantityPerOrder": 1,
      "minimumQuantity": 1,
      "name": "Ava Chen",
      "onSaleStatus": "string",
      "orderConfirmationMessage": {},
      "quantitySold": 1,
      "quantityTotal": 1,
      "resourceUri": "string",
      "salesChannels": [
        "string"
      ],
      "salesEnd": "string",
      "salesEndRelative": {},
      "salesStart": "string",
      "secondaryAssignmentEnabled": true,
      "sorting": 1,
      "splitFee": true,
      "tax": {},
      "ticketParentId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualCost` | object |  |
| `actualFee` | object |  |
| `autoHide` | boolean |  |
| `capacity` | number |  |
| `category` | string |  |
| `cost` | object |  |
| `deliveryMethods[]` | string |  |
| `description` | object |  |
| `displayName` | string |  |
| `donation` | boolean |  |
| `eventId` | string |  |
| `fee` | object |  |
| `free` | boolean |  |
| `hasPdfTicket` | boolean |  |
| `hidden` | boolean |  |
| `hiddenCurrently` | boolean |  |
| `hideDescription` | boolean |  |
| `hideSaleDates` | boolean |  |
| `id` | string |  |
| `imageId` | object |  |
| `includeFee` | boolean |  |
| `maximumQuantity` | object |  |
| `maximumQuantityPerOrder` | number |  |
| `minimumQuantity` | number |  |
| `name` | string |  |
| `onSaleStatus` | string |  |
| `orderConfirmationMessage` | object |  |
| `quantitySold` | number |  |
| `quantityTotal` | number |  |
| `resourceUri` | string |  |
| `salesChannels[]` | string |  |
| `salesEnd` | string |  |
| `salesEndRelative` | object |  |
| `salesStart` | string |  |
| `secondaryAssignmentEnabled` | boolean |  |
| `sorting` | number |  |
| `splitFee` | boolean |  |
| `tax` | object |  |
| `ticketParentId` | object |  |

## Native endpoint

Through the native Eventbrite API, this operation is `POST /events/:eventId/ticket_classes/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-ticket-class.md) for the provider-specific parameters and requirements.

