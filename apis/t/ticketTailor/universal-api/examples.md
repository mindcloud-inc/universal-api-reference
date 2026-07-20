# Ticket Tailor Universal API Examples

These examples use the MindCloud API key and Ticket Tailor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events

Retrieves box office events from Ticket Tailor.

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

Example response:

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

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ticketTailor/latest/actions/list-events).
