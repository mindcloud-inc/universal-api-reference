# Eventbrite: List Event Ticket Classes

Retrieves event ticket classes from Eventbrite.

```
GET https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-event-ticket-classes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-event-ticket-classes?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-event-ticket-classes?${params}`, {
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

Through the native Eventbrite API, this operation is `GET /events/:eventId/ticket_classes/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-ticket-classes.md) for the provider-specific parameters and requirements.

