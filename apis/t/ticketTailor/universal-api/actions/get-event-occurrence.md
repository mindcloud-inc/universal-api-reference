# Ticket Tailor: Get Event Occurrence

Retrieves an event occurrence from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/get-event-occurrence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/get-event-occurrence?connectionId=$CONNECTION_ID&eventSeriesId=string&eventOccurrenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventSeriesId": "string",
  "eventOccurrenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/get-event-occurrence?${params}`, {
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
| `eventSeriesId` | string | yes | Ticket Tailor event series ID. |
| `eventOccurrenceId` | string | yes | Ticket Tailor event occurrence ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableStatus": "string",
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
      "chk": "string",
      "currency": "string",
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
      "maxTicketsSoldPerOccurrence": 1,
      "object": "string",
      "onlineLink": "https://example.com",
      "overrideId": "string",
      "revenue": 1,
      "salesTaxLabel": "string",
      "salesTaxPercentage": 1,
      "salesTaxTreatment": "string",
      "start": {
        "date": "string",
        "formatted": "string",
        "iso": "string",
        "time": "string",
        "timezone": "string",
        "unix": 1
      },
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
      "totalIssuedTickets": 1,
      "transactionFeeFixedAmount": 1,
      "transactionFeePercentage": 1,
      "unavailable": "string",
      "unavailableStatus": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableStatus` | string | Optional custom status message when event is set to be available |
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
| `chk` | string | Used for Ticket Tailor checkout chk value |
| `currency` | string | Information about the currency the event is configured to use |
| `end` | object | The end date and time for the event |
| `end.date` | string | ISO-8601 date for the end of the event |
| `end.formatted` | string | A formatted date string for the end of the event |
| `end.iso` | string | ISO-8601 date and time for the end of the event |
| `end.time` | string | Time of the end of the event |
| `end.timezone` | string | Timezone offset for the end of the event |
| `end.unix` | number | Unix timestamp for for the end of the event |
| `eventSeriesId` | string | A unique identifier for the associated event series |
| `hidden` | string | True, if event is set to hidden |
| `id` | string | A unique identifier for the event occurrence |
| `maxTicketsSoldPerOccurrence` | number | Maximum quantity of tickets that can be sold across all ticket types |
| `object` | string |  |
| `onlineLink` | string | URL of the online event |
| `overrideId` | string | A unique identifier for the associated override |
| `revenue` | number | Total revenue of the event |
| `salesTaxLabel` | string | The label for the sales tax |
| `salesTaxPercentage` | number | The percentage of the sales tax |
| `salesTaxTreatment` | string | The treatment of the sales tax |
| `start` | object | The start date and time for the event |
| `start.date` | string | ISO-8601 date for the start of the event |
| `start.formatted` | string | A formatted date string for the start of the event |
| `start.iso` | string | ISO-8601 date and time for the start of the event |
| `start.time` | string | Time of the start of the event |
| `start.timezone` | string | Timezone offset for the start of the event |
| `start.unix` | number | Unix timestamp for the start of the event |
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
| `totalIssuedTickets` | number | Total number of issued tickets |
| `transactionFeeFixedAmount` | number | Fixed amount of the transaction fee |
| `transactionFeePercentage` | number | Percentage of the transaction fee |
| `unavailable` | string | True, if event is set to unavailable |
| `unavailableStatus` | string | Optional custom status message when event is set to be unavailable |
| `url` | string | Event occurrence URL |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/event_series/:event_series_id/events/:event_occurrence_id` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-occurrence.md) for the provider-specific parameters and requirements.

