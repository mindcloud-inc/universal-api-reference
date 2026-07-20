# Ticket Tailor: List Event Series

Retrieves box office event series from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-event-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-event-series?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-event-series?${params}`, {
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
      "bundles": [
        {
          "accessCode": "string",
          "bookingFee": 1,
          "description": "string",
          "groupId": "string",
          "id": "string",
          "name": "Ava Chen",
          "object": "string",
          "price": 1,
          "products": [
            {
              "id": "string",
              "quantity": 1
            }
          ],
          "status": "string",
          "ticketTypes": [
            {
              "id": "string",
              "quantity": 1
            }
          ]
        }
      ],
      "callToAction": "string",
      "createdAt": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      },
      "currency": "string",
      "defaultMaxTicketsSoldPerOccurrence": 1,
      "defaultTicketGroups": [
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
      "defaultTicketTypes": [
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
      "description": "string",
      "id": "string",
      "images": {
        "header": "string",
        "thumbnail": "string"
      },
      "name": "Ava Chen",
      "nextOccurrenceDate": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      },
      "object": "string",
      "onlineEvent": "string",
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
      "status": "string",
      "ticketsAvailableAt": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      },
      "ticketsAvailableAtMessage": "string",
      "ticketsUnavailableAt": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      },
      "ticketsUnavailableAtMessage": "string",
      "timezone": "string",
      "totalIssuedTickets": 1,
      "totalOccurrences": 1,
      "transactionFeeFixedAmount": 1,
      "transactionFeePercentage": 1,
      "upcomingOccurrences": 1,
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
| `accessCode` | string | Code to access a protected event series |
| `bundles` | array<object> | List of associated bundles |
| `bundles[].accessCode` | string | Code to access a bundle |
| `bundles[].bookingFee` | number | Booking fee in cents |
| `bundles[].description` | string | Bundle description |
| `bundles[].groupId` | string | Bundle group ID |
| `bundles[].id` | string |  |
| `bundles[].name` | string | Bundle name |
| `bundles[].object` | string |  |
| `bundles[].price` | number | Price in cents |
| `bundles[].products` | array<object> | Array of associated products |
| `bundles[].products[].id` | string | A unique product identifier |
| `bundles[].products[].quantity` | number | Product quantity |
| `bundles[].status` | string | Bundle status |
| `bundles[].ticketTypes` | array<object> | Array of associated ticket types |
| `bundles[].ticketTypes[].id` | string | A unique ticket type identifier |
| `bundles[].ticketTypes[].quantity` | number | Ticket type quantity |
| `callToAction` | string | Call to action text used on the event series page |
| `createdAt` | object | Date and time when the event series were created |
| `createdAt.date` | string | ISO-8601 date for the end of the event |
| `createdAt.formatted` | string | A formatted date string for the end of the event |
| `createdAt.iso` | string | ISO-8601 date and time for the end of the event |
| `createdAt.time` | string | Time of the end of the event |
| `createdAt.timezone` | string | Timezone offset for the end of the event |
| `createdAt.unix` | number | Unix timestamp for for the end of the event |
| `currency` | string | Information about the currency the event series is configured to use |
| `defaultMaxTicketsSoldPerOccurrence` | number | Maximum quantity of tickets that can be sold across all ticket types |
| `defaultTicketGroups` | array<object> | Ticket groups that are not overridden |
| `defaultTicketGroups[].bundleIds` | array<string> | An array of associated bundle ids |
| `defaultTicketGroups[].id` | string | A unique identifier for the ticket group |
| `defaultTicketGroups[].maxPerOrder` | number | Maximum number of tickets allowed per order |
| `defaultTicketGroups[].maxQuantity` | number | Maximum quantity of tickets that are allowed to be sold for the tickets in the group |
| `defaultTicketGroups[].minPerOrder` | number | Minimum number of tickets allowed per order |
| `defaultTicketGroups[].name` | string | Name of the ticket group |
| `defaultTicketGroups[].object` | string |  |
| `defaultTicketGroups[].sortOrder` | number | Sort index of the group in the UI |
| `defaultTicketGroups[].ticketIds` | array<string> | An array of associated ticket type ids |
| `defaultTicketTypes` | array<object> | Ticket types that are not overridden |
| `defaultTicketTypes[].accessCode` | string | Code to access a hidden ticket |
| `defaultTicketTypes[].bookingFee` | number | Optional booking fee which is charged per ticket type to the customer and the funds are paid to you. |
| `defaultTicketTypes[].description` | string |  |
| `defaultTicketTypes[].discounts` | array<string> | An array of associated discounts |
| `defaultTicketTypes[].groupId` | string | ID of the group this ticket type belongs to |
| `defaultTicketTypes[].hasOverrides` | string | Specifies whether the ticket type has overrides |
| `defaultTicketTypes[].hideAfter` | object | Timestamp in seconds when the ticket type should be hidden until. |
| `defaultTicketTypes[].hideAfter.date` | string | ISO-8601 date for the start of the event |
| `defaultTicketTypes[].hideAfter.formatted` | string | A formatted date string for the start of the event |
| `defaultTicketTypes[].hideAfter.iso` | string | ISO-8601 date and time for the start of the event |
| `defaultTicketTypes[].hideAfter.time` | string | Time for the start of the event |
| `defaultTicketTypes[].hideAfter.timezone` | string | Timezone offset for the start of the event |
| `defaultTicketTypes[].hideAfter.unix` | number | Unix timestamp for the start of the event |
| `defaultTicketTypes[].hideUntil` | object | Timestamp in seconds when the ticket type should be hidden after. |
| `defaultTicketTypes[].hideUntil.date` | string | ISO-8601 date for the start of the event |
| `defaultTicketTypes[].hideUntil.formatted` | string | A formatted date string for the start of the event |
| `defaultTicketTypes[].hideUntil.iso` | string | ISO-8601 date and time for the start of the event |
| `defaultTicketTypes[].hideUntil.time` | string | Time for the start of the event |
| `defaultTicketTypes[].hideUntil.timezone` | string | Timezone offset for the start of the event |
| `defaultTicketTypes[].hideUntil.unix` | number | Unix timestamp for the start of the event |
| `defaultTicketTypes[].hideWhenSoldOut` | string | Specifies whether the ticket is hidden when it has sold out |
| `defaultTicketTypes[].id` | string | A unique identifier for the ticket type |
| `defaultTicketTypes[].maxPerOrder` | number | Maximum number of ticket types you can select per order |
| `defaultTicketTypes[].minPerOrder` | number | Minimum number of ticket types you can select per order |
| `defaultTicketTypes[].name` | string | Name of the ticket type |
| `defaultTicketTypes[].object` | string |  |
| `defaultTicketTypes[].overrideId` | string | The ID of the override associated with the ticket type |
| `defaultTicketTypes[].price` | number | Cost of the ticket type |
| `defaultTicketTypes[].quantity` | number | Number available for purchase |
| `defaultTicketTypes[].quantityHeld` | number | Number held |
| `defaultTicketTypes[].quantityInBaskets` | number | Number in baskets |
| `defaultTicketTypes[].quantityIssued` | number | Number issued |
| `defaultTicketTypes[].quantityTotal` | number | Total number including issued and still available |
| `defaultTicketTypes[].showQuantityRemaining` | string | Specifies whether to show the number of tickets still available |
| `defaultTicketTypes[].showQuantityRemainingLessThan` | number | Only show number of tickets still available when the available quantity is equal to or lower than this threshold |
| `defaultTicketTypes[].sortOrder` | number | Sort index of ticket type in the UI |
| `defaultTicketTypes[].status` | string | Status of the ticket type |
| `defaultTicketTypes[].type` | string |  |
| `description` | string | Description of the event series |
| `id` | string | A unique identifier for the event series |
| `images` | object | Imagages that have been uploaded to this event series |
| `images.header` | string | Image URL of the header image used on the event series page |
| `images.thumbnail` | string | Image URL of the thumbnail used on the event series page |
| `name` | string | Name of the event series |
| `nextOccurrenceDate` | object | Date and time when the next event in the series happens |
| `nextOccurrenceDate.date` | string | ISO-8601 date for the end of the event |
| `nextOccurrenceDate.formatted` | string | A formatted date string for the end of the event |
| `nextOccurrenceDate.iso` | string | ISO-8601 date and time for the end of the event |
| `nextOccurrenceDate.time` | string | Time of the end of the event |
| `nextOccurrenceDate.timezone` | string | Timezone offset for the end of the event |
| `nextOccurrenceDate.unix` | number | Unix timestamp for for the end of the event |
| `object` | string |  |
| `onlineEvent` | string | Returns whether or not the event is online |
| `paymentMethods` | array<object> | An array of payment methods |
| `paymentMethods[].externalId` | string | A unique identifier for the payment method |
| `paymentMethods[].id` | string | A unique identifier for internal payment methods |
| `paymentMethods[].instructions` | string | Instructions for the customer on how to pay. Used for offline payments. |
| `paymentMethods[].name` | string | Name of the payment method |
| `paymentMethods[].type` | string | The type of payment method |
| `private` | string | Returns whether or not the event is private |
| `revenue` | number | Total revenue of the event series |
| `salesTaxLabel` | string | The label for the sales tax |
| `salesTaxPercentage` | number | The percentage of the sales tax |
| `salesTaxTreatment` | string | The treatment of the sales tax |
| `showMap` | string | Returns whether or not the map should be shown on the event series page. It depends if venue location is set and if the event is not online and hide map is not set in the event series. |
| `status` | string | Status of the event |
| `ticketsAvailableAt` | object | Date when tickets become available for purchase |
| `ticketsAvailableAt.date` | string | ISO-8601 date for the end of the event |
| `ticketsAvailableAt.formatted` | string | A formatted date string for the end of the event |
| `ticketsAvailableAt.iso` | string | ISO-8601 date and time for the end of the event |
| `ticketsAvailableAt.time` | string | Time of the end of the event |
| `ticketsAvailableAt.timezone` | string | Timezone offset for the end of the event |
| `ticketsAvailableAt.unix` | number | Unix timestamp for for the end of the event |
| `ticketsAvailableAtMessage` | string | Message to show when tickets are not yet available to purchase. {countdown} is replaced with time remaining until tickets become available |
| `ticketsUnavailableAt` | object | Date when tickets become unavailable for purchase |
| `ticketsUnavailableAt.date` | string | ISO-8601 date for the end of the event |
| `ticketsUnavailableAt.formatted` | string | A formatted date string for the end of the event |
| `ticketsUnavailableAt.iso` | string | ISO-8601 date and time for the end of the event |
| `ticketsUnavailableAt.time` | string | Time of the end of the event |
| `ticketsUnavailableAt.timezone` | string | Timezone offset for the end of the event |
| `ticketsUnavailableAt.unix` | number | Unix timestamp for for the end of the event |
| `ticketsUnavailableAtMessage` | string | Message to show when tickets are unavailable to purchase |
| `timezone` | string | TZ format timezone string |
| `totalIssuedTickets` | number | Total number of issued tickets |
| `totalOccurrences` | number | Total number of time the event series occurs |
| `transactionFeeFixedAmount` | number | Fixed amount of the transaction fee |
| `transactionFeePercentage` | number | Percentage of the transaction fee |
| `upcomingOccurrences` | number | The number of upcoming occurrences of the event series |
| `url` | string | Event series URL |
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

Through the native Ticket Tailor API, this operation is `GET /v1/event_series` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-event-series.md) for the provider-specific parameters and requirements.

