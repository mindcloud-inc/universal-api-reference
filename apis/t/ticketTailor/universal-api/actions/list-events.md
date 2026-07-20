# Ticket Tailor: List Events

Retrieves box office events from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accessCode": "string",
      "availableStatus": "string",
      "callToAction": "string",
      "checkoutUrl": "https://example.com",
      "chk": "string",
      "createdAt": 1,
      "currency": "string",
      "description": "string",
      "end": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      },
      "eventSeriesId": "string",
      "hidden": "string",
      "id": "string",
      "images": {
        "header": "string",
        "thumbnail": "string"
      },
      "maxTicketsSoldPerOccurrence": 1,
      "name": "Ava Chen",
      "object": "string",
      "onlineEvent": "string",
      "onlineLink": "https://example.com",
      "overrideId": 1,
      "paymentMethods": [
        {
          "externalId": "string",
          "id": "string",
          "instructions": "string",
          "name": "Ava Chen",
          "type": "string"
        }
      ],
      "private": "string",
      "revenue": 1,
      "salesTaxLabel": "string",
      "salesTaxPercentage": 1,
      "salesTaxTreatment": "string",
      "showMap": "string",
      "start": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      },
      "status": "string",
      "ticketGroups": [
        {
          "bundleIds": [
            "string"
          ],
          "id": "string",
          "maxPerOrder": 1,
          "maxQuantity": 1,
          "minPerOrder": 1,
          "name": "Ava Chen",
          "object": "string",
          "sortOrder": 1,
          "ticketIds": [
            "string"
          ]
        }
      ],
      "ticketsAvailable": "string",
      "ticketsAvailableAt": 1,
      "ticketsAvailableAtMessage": "string",
      "ticketsUnavailableAt": 1,
      "ticketsUnavailableAtMessage": "string",
      "ticketTypes": [
        {
          "accessCode": "string",
          "bookingFee": 1,
          "description": "string",
          "discounts": [
            "string"
          ],
          "groupId": "string",
          "hasOverrides": "string",
          "hideAfter": {
            "date": "string",
            "formatted": "string",
            "iso": "string",
            "time": "string",
            "timezone": "string",
            "unix": 1
          },
          "hideUntil": {
            "date": "string",
            "formatted": "string",
            "iso": "string",
            "time": "string",
            "timezone": "string",
            "unix": 1
          },
          "hideWhenSoldOut": "string",
          "id": "string",
          "maxPerOrder": 1,
          "minPerOrder": 1,
          "name": "Ava Chen",
          "object": "string",
          "overrideId": "string",
          "price": 1,
          "quantity": 1,
          "quantityHeld": 1,
          "quantityInBaskets": 1,
          "quantityIssued": 1,
          "quantityTotal": 1,
          "showQuantityRemaining": "string",
          "showQuantityRemainingLessThan": 1,
          "sortOrder": 1,
          "status": "string",
          "type": "string"
        }
      ],
      "timezone": "string",
      "totalHolds": 1,
      "totalIssuedTickets": 1,
      "totalOrders": 1,
      "transactionFeeFixedAmount": 1,
      "transactionFeePercentage": 1,
      "unavailable": "string",
      "unavailableStatus": "string",
      "url": "https://example.com",
      "venue": {
        "country": "string",
        "name": "Ava Chen",
        "postalCode": "string"
      },
      "voucherIds": [
        "string"
      ],
      "waitlistActive": "string",
      "waitlistCallToAction": "string",
      "waitlistConfirmationMessage": "string",
      "waitlistEventPageText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessCode` | string | Code to access a protected event |
| `availableStatus` | string | Optional custom status message when event is set to be available |
| `callToAction` | string | Call to action text used on the event page |
| `checkoutUrl` | string | Event checkout URL |
| `chk` | string | Used for Ticket Tailor checkout chk value |
| `createdAt` | number |  |
| `currency` | string | Information about the currency the event is configured to use |
| `description` | string | Description of the event |
| `end` | object |  |
| `end.date` | string | ISO-8601 date for the end of the event |
| `end.formatted` | string | A formatted date string for the end of the event |
| `end.iso` | string | ISO-8601 date and time for the end of the event |
| `end.time` | string | Time of the end of the event |
| `end.timezone` | string | Timezone offset for the end of the event |
| `end.unix` | number | Unix timestamp for for the end of the event |
| `eventSeriesId` | string | Recurring events are grouped by an event_series_id |
| `hidden` | string | True, if event is set to hidden |
| `id` | string | A unique identifier for the event |
| `images` | object | Images that have been uploaded to this event |
| `images.header` | string | Image URL of the header image used on your event page |
| `images.thumbnail` | string | Image URL of the thumbnail used on your event page |
| `maxTicketsSoldPerOccurrence` | number | Maximum quantity of tickets that can be sold across all ticket types |
| `name` | string | Name of the event |
| `object` | string |  |
| `onlineEvent` | string | Returns whether or not the event is online |
| `onlineLink` | string | URL of the online event |
| `overrideId` | number | A unique identifier for the associated override |
| `paymentMethods` | array<object> | An array of payment methods |
| `paymentMethods[].externalId` | string | A unique identifier for the payment method |
| `paymentMethods[].id` | string | A unique identifier for internal payment methods |
| `paymentMethods[].instructions` | string | Instructions for the customer on how to pay. Used for offline payments. |
| `paymentMethods[].name` | string | Name of the payment method |
| `paymentMethods[].type` | string | The type of payment method |
| `private` | string | Returns whether or not the event is private |
| `revenue` | number | Total revenue of the event |
| `salesTaxLabel` | string | The label for the sales tax |
| `salesTaxPercentage` | number | The percentage of the sales tax |
| `salesTaxTreatment` | string | The treatment of the sales tax |
| `showMap` | string | Returns whether or not the map should be shown on the event page. It depends if venue location is set and if the event is not online and hide map is not set in the event series. |
| `start` | object |  |
| `start.date` | string | ISO-8601 date for the start of the event |
| `start.formatted` | string | A formatted date string for the start of the event |
| `start.iso` | string | ISO-8601 date and time for the start of the event |
| `start.time` | string | Time of the start of the event |
| `start.timezone` | string | Timezone offset for the start of the event |
| `start.unix` | number | Unix timestamp for the start of the event |
| `status` | string | Status of the event |
| `ticketGroups` | array<object> |  |
| `ticketGroups[].bundleIds` | array<string> | An array of associated bundle ids |
| `ticketGroups[].id` | string | A unique identifier for the ticket group |
| `ticketGroups[].maxPerOrder` | number | Maximum number of tickets allowed per order |
| `ticketGroups[].maxQuantity` | number | Maximum quantity of tickets that are allowed to be sold for the tickets in the group |
| `ticketGroups[].minPerOrder` | number | Minimum number of tickets allowed per order |
| `ticketGroups[].name` | string | Name of the ticket group |
| `ticketGroups[].object` | string |  |
| `ticketGroups[].sortOrder` | number | Sort index of the group in the UI |
| `ticketGroups[].ticketIds` | array<string> | An array of associated ticket type ids |
| `ticketsAvailable` | string | Are there any ticket types available? |
| `ticketsAvailableAt` | number | Timestamp in UTC in seconds when tickets become available for purchase |
| `ticketsAvailableAtMessage` | string | Message to show when tickets are not yet available to purchase. {countdown} is replaced with time remaining until tickets become available |
| `ticketsUnavailableAt` | number | Timestamp in UTC in seconds when tickets become unavailable for purchase |
| `ticketsUnavailableAtMessage` | string | Message to show when tickets are unavailable to purchase |
| `ticketTypes` | array<object> |  |
| `ticketTypes[].accessCode` | string | Code to access a hidden ticket |
| `ticketTypes[].bookingFee` | number | Optional booking fee which is charged per ticket type to the customer and the funds are paid to you. |
| `ticketTypes[].description` | string |  |
| `ticketTypes[].discounts` | array<string> | An array of associated discounts |
| `ticketTypes[].groupId` | string | ID of the group this ticket type belongs to |
| `ticketTypes[].hasOverrides` | string | Specifies whether the ticket type has overrides |
| `ticketTypes[].hideAfter` | object | Timestamp in seconds when the ticket type should be hidden until. |
| `ticketTypes[].hideAfter.date` | string | ISO-8601 date for the start of the event |
| `ticketTypes[].hideAfter.formatted` | string | A formatted date string for the start of the event |
| `ticketTypes[].hideAfter.iso` | string | ISO-8601 date and time for the start of the event |
| `ticketTypes[].hideAfter.time` | string | Time for the start of the event |
| `ticketTypes[].hideAfter.timezone` | string | Timezone offset for the start of the event |
| `ticketTypes[].hideAfter.unix` | number | Unix timestamp for the start of the event |
| `ticketTypes[].hideUntil` | object | Timestamp in seconds when the ticket type should be hidden after. |
| `ticketTypes[].hideUntil.date` | string | ISO-8601 date for the start of the event |
| `ticketTypes[].hideUntil.formatted` | string | A formatted date string for the start of the event |
| `ticketTypes[].hideUntil.iso` | string | ISO-8601 date and time for the start of the event |
| `ticketTypes[].hideUntil.time` | string | Time for the start of the event |
| `ticketTypes[].hideUntil.timezone` | string | Timezone offset for the start of the event |
| `ticketTypes[].hideUntil.unix` | number | Unix timestamp for the start of the event |
| `ticketTypes[].hideWhenSoldOut` | string | Specifies whether the ticket is hidden when it has sold out |
| `ticketTypes[].id` | string | A unique identifier for the ticket type |
| `ticketTypes[].maxPerOrder` | number | Maximum number of ticket types you can select per order |
| `ticketTypes[].minPerOrder` | number | Minimum number of ticket types you can select per order |
| `ticketTypes[].name` | string | Name of the ticket type |
| `ticketTypes[].object` | string |  |
| `ticketTypes[].overrideId` | string | The ID of the override associated with the ticket type |
| `ticketTypes[].price` | number | Cost of the ticket type |
| `ticketTypes[].quantity` | number | Number available for purchase |
| `ticketTypes[].quantityHeld` | number | Number held |
| `ticketTypes[].quantityInBaskets` | number | Number in baskets |
| `ticketTypes[].quantityIssued` | number | Number issued |
| `ticketTypes[].quantityTotal` | number | Total number including issued and still available |
| `ticketTypes[].showQuantityRemaining` | string | Specifies whether to show the number of tickets still available |
| `ticketTypes[].showQuantityRemainingLessThan` | number | Only show number of tickets still available when the available quantity is equal to or lower than this threshold |
| `ticketTypes[].sortOrder` | number | Sort index of ticket type in the UI |
| `ticketTypes[].status` | string | Status of the ticket type |
| `ticketTypes[].type` | string |  |
| `timezone` | string | TZ format timezone string |
| `totalHolds` | number | Total number of holds |
| `totalIssuedTickets` | number | Total number of issued tickets |
| `totalOrders` | number | Total number of orders |
| `transactionFeeFixedAmount` | number | Fixed amount of the transaction fee |
| `transactionFeePercentage` | number | Percentage of the transaction fee |
| `unavailable` | string | True, if event is set to unavailable |
| `unavailableStatus` | string | optional custom status message when event is set to be unavailable |
| `url` | string | Event page URL |
| `venue` | object |  |
| `venue.country` | string | Country of the venue |
| `venue.name` | string | Name of the venue |
| `venue.postalCode` | string | Postal code of the venue |
| `voucherIds` | array<string> | List of voucher IDs |
| `waitlistActive` | string | Indicates whether waitlist is enabled for the event series |
| `waitlistCallToAction` | string | The text displayed on event action buttons and as a title above the waitlist format |
| `waitlistConfirmationMessage` | string | Text shown to the user after they have signed up to the waitlist |
| `waitlistEventPageText` | string | Description above ticket waitlist form |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/events` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

