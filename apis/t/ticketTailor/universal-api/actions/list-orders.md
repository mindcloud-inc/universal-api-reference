# Ticket Tailor: List Orders

Retrieves box office orders from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-orders?${params}`, {
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
      "buyerDetails": {
        "address": {
          "address1": "string",
          "address2": "string",
          "address3": "string",
          "postalCode": "string"
        },
        "customQuestions": [
          {
            "answer": "string",
            "question": "string"
          }
        ],
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen",
        "phone": "string"
      },
      "createdAt": 1,
      "creditedOutAmount": 1,
      "currency": {
        "baseMultiplier": 1,
        "code": "string"
      },
      "eventSummary": {
        "endDate": {
          "date": "string",
          "formatted": "string",
          "iso": "string",
          "time": "string",
          "timezone": "string",
          "unix": 1
        },
        "eventId": "string",
        "eventSeriesId": "string",
        "id": "string",
        "name": "Ava Chen",
        "startDate": {
          "date": "string",
          "formatted": "string",
          "iso": "string",
          "time": "string",
          "timezone": "string",
          "unix": 1
        },
        "venue": {
          "country": "string",
          "name": "Ava Chen",
          "postalCode": "string"
        }
      },
      "id": "string",
      "issuedTickets": [
        {
          "addOnId": "string",
          "barcode": "string",
          "barcodeUrl": "https://example.com",
          "checkedIn": "string",
          "createdAt": 1,
          "customQuestions": [
            {
              "answer": "string",
              "question": "string"
            }
          ],
          "description": "string",
          "email": "ava@example.com",
          "eventId": "string",
          "eventSeriesId": "string",
          "firstName": "Ava",
          "fullName": "Ava Chen",
          "groupTicketBarcode": "string",
          "id": "string",
          "lastName": "Chen",
          "listedCurrency": {
            "baseMultiplier": 1,
            "code": "string"
          },
          "listedPrice": 1,
          "object": "string",
          "orderId": "string",
          "qrCodeUrl": "https://example.com",
          "reference": "string",
          "reservation": "string",
          "source": "string",
          "status": "string",
          "ticketTypeId": "string",
          "updatedAt": 1,
          "voidedAt": 1
        }
      ],
      "lineItems": [
        {
          "bookingFee": 1,
          "description": "string",
          "id": "string",
          "itemId": "string",
          "object": "string",
          "quantity": 1,
          "storeId": "string",
          "total": 1,
          "type": "string",
          "value": 1
        }
      ],
      "marketingOptIn": "string",
      "metaData": [
        {
          "key": "string",
          "value": "string"
        }
      ],
      "notes": "string",
      "object": "string",
      "paymentMethod": {
        "externalId": "string",
        "id": "string",
        "instructions": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "referralTag": "string",
      "refundAmount": 1,
      "refundedVoucherId": 1,
      "soldProducts": [
        {
          "eventId": "string",
          "fulfilment": "string",
          "fulfilmentReferenceId": "string",
          "fulfilmentReferenceName": "Ava Chen",
          "id": "string",
          "object": "string",
          "orderId": "string",
          "productId": "string",
          "productName": "Ava Chen",
          "salesChannel": "string",
          "salesChannelReferenceName": "Ava Chen",
          "status": "string",
          "storeId": 1
        }
      ],
      "status": "string",
      "statusMessage": "string",
      "subtotal": 1,
      "tax": 1,
      "taxTreatment": "string",
      "total": 1,
      "totalPaid": 1,
      "txnId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buyerDetails` | object | Information buyer provided in the checkout |
| `buyerDetails.address` | object | Information about buyer address |
| `buyerDetails.address.address1` | string | First line of address |
| `buyerDetails.address.address2` | string | Second line of address |
| `buyerDetails.address.address3` | string | Third line of address |
| `buyerDetails.address.postalCode` | string | Postal code, zip code or postcode |
| `buyerDetails.customQuestions` | array<object> | Buyer provided answers to custom questions in checkout |
| `buyerDetails.customQuestions[].answer` | string |  |
| `buyerDetails.customQuestions[].question` | string |  |
| `buyerDetails.email` | string | Buyer email address |
| `buyerDetails.firstName` | string | Buyer first name |
| `buyerDetails.lastName` | string | Buyer last name |
| `buyerDetails.name` | string | Buyer full name |
| `buyerDetails.phone` | string | Buyer phone number |
| `createdAt` | number | Order creation timestamp |
| `creditedOutAmount` | number | Refunded amount issued as credit in cents |
| `currency` | object | Information about order currency |
| `currency.baseMultiplier` | number | Base multiplier for conversions |
| `currency.code` | string | Currency used for purchase |
| `eventSummary` | object | Short event summary this order was made for |
| `eventSummary.endDate` | object | The end date for the event in various formats |
| `eventSummary.endDate.date` | string | ISO-8601 date for the end of the event |
| `eventSummary.endDate.formatted` | string | A formatted date string for the end of the event |
| `eventSummary.endDate.iso` | string | ISO-8601 date and time for the end of the event |
| `eventSummary.endDate.time` | string | Time for the end of the event |
| `eventSummary.endDate.timezone` | string | Timezone offset for the end of the event |
| `eventSummary.endDate.unix` | number | Unix timestamp for the end of the event |
| `eventSummary.eventId` | string | ID of the event occurrence an order belongs to |
| `eventSummary.eventSeriesId` | string | ID of the event series an order belongs to |
| `eventSummary.id` | string | ID of the event occurrence an order belongs to (deprecated) |
| `eventSummary.name` | string | Name of the event |
| `eventSummary.startDate` | object | The start date for the event in various formats |
| `eventSummary.startDate.date` | string | ISO-8601 date for the start of the event |
| `eventSummary.startDate.formatted` | string | A formatted date string for the start of the event |
| `eventSummary.startDate.iso` | string | ISO-8601 date and time for the start of the event |
| `eventSummary.startDate.time` | string | Time for the start of the event |
| `eventSummary.startDate.timezone` | string | Timezone offset for the start of the event |
| `eventSummary.startDate.unix` | number | Unix timestamp for the start of the event |
| `eventSummary.venue` | object | The venue information for the event |
| `eventSummary.venue.country` | string | Country of the venue |
| `eventSummary.venue.name` | string | The name of the venue |
| `eventSummary.venue.postalCode` | string | The postcode of the venue for this event |
| `id` | string | A unique identifier for the order |
| `issuedTickets` | array<object> | Issued tickets for order |
| `issuedTickets[].addOnId` | string | A unique identifier for the associated product |
| `issuedTickets[].barcode` | string | Barcode text value |
| `issuedTickets[].barcodeUrl` | string | URL to barcode image |
| `issuedTickets[].checkedIn` | string | Returns whether or not issued ticket is checked in |
| `issuedTickets[].createdAt` | number | Timestamp when issued ticket was created |
| `issuedTickets[].customQuestions` | array<object> | Buyer provided answers to custom questions in checkout |
| `issuedTickets[].customQuestions[].answer` | string |  |
| `issuedTickets[].customQuestions[].question` | string |  |
| `issuedTickets[].description` | string |  |
| `issuedTickets[].email` | string | The order email address |
| `issuedTickets[].eventId` | string | ID of the event issued ticket belongs to |
| `issuedTickets[].eventSeriesId` | string | ID of the event series the issued ticket belongs to |
| `issuedTickets[].firstName` | string | First name of attendee |
| `issuedTickets[].fullName` | string | Full name of attendee |
| `issuedTickets[].groupTicketBarcode` | string | Barcode for group ticket, if it is part of one |
| `issuedTickets[].id` | string | A unique identifier for the issued ticket |
| `issuedTickets[].lastName` | string | Last name of attendee |
| `issuedTickets[].listedCurrency` | object | List currency of the ticket type at the time of purchase |
| `issuedTickets[].listedCurrency.baseMultiplier` | number |  |
| `issuedTickets[].listedCurrency.code` | string |  |
| `issuedTickets[].listedPrice` | number | List price of the ticket type at the time of purchase |
| `issuedTickets[].object` | string |  |
| `issuedTickets[].orderId` | string | A unique identifier for the order |
| `issuedTickets[].qrCodeUrl` | string | URL to QR code image |
| `issuedTickets[].reference` | string | An external reference for imported tickets (via the API or Dashboard) |
| `issuedTickets[].reservation` | string | Reservation from seating chart where applicable |
| `issuedTickets[].source` | string |  |
| `issuedTickets[].status` | string |  |
| `issuedTickets[].ticketTypeId` | string | ID of the ticket type |
| `issuedTickets[].updatedAt` | number | Timestamp when issued ticket was last updated |
| `issuedTickets[].voidedAt` | number | Timestamp when issued ticket was voided |
| `lineItems` | array<object> |  |
| `lineItems[].bookingFee` | number | Optional booking fee which is charged per ticket type to the customer and the funds are paid to you. |
| `lineItems[].description` | string | Basket item description |
| `lineItems[].id` | string | A unique identifier for the basket item |
| `lineItems[].itemId` | string | The line item type id with a prefix. |
| `lineItems[].object` | string |  |
| `lineItems[].quantity` | number | Amount of line item objects |
| `lineItems[].storeId` | string | The store id prefixed with 'st_' |
| `lineItems[].total` | number | Total amount including tax for line item |
| `lineItems[].type` | string | `ticket` is a purchased ticket, `transaction_charge` is a transaction fee to orders. This is charged once per order as opposed to ticket booking fees which are charged once per ticket. `void` means ticket was voided after the purchase, `tax` is sales tax eg. VAT, `gift_card` is discount or voucher applied and `donation` is for donating value |
| `lineItems[].value` | number | Amount without tax |
| `marketingOptIn` | string | Whether the buyer opted in to receive marketing emails |
| `metaData` | array<object> | Meta data attached to the order |
| `metaData[].key` | string |  |
| `metaData[].value` | string |  |
| `notes` | string | Notes attached to the order |
| `object` | string |  |
| `paymentMethod` | object |  |
| `paymentMethod.externalId` | string | A unique identifier for the payment method |
| `paymentMethod.id` | string | A unique identifier for internal payment methods |
| `paymentMethod.instructions` | string | Instructions for the customer on how to pay. Used for offline payments. |
| `paymentMethod.name` | string | Name of the payment method |
| `paymentMethod.type` | string | The type of payment method |
| `referralTag` | string | A unique tag to track where sales originated |
| `refundAmount` | number | Refunded amount in cents |
| `refundedVoucherId` | number | The unique identifier for the existing voucher |
| `soldProducts` | array<object> | Sold products for order |
| `soldProducts[].eventId` | string | ID of the event if sold through event sales channel |
| `soldProducts[].fulfilment` | string | Type of fulfilment for this product |
| `soldProducts[].fulfilmentReferenceId` | string | Prefixed ID of the issued ticket (it_), membership (im_), or voucher (vo_) if fulfilled |
| `soldProducts[].fulfilmentReferenceName` | string | Name/label of the fulfilment reference |
| `soldProducts[].id` | string | A unique identifier for the sold product |
| `soldProducts[].object` | string |  |
| `soldProducts[].orderId` | string | A unique identifier for the order |
| `soldProducts[].productId` | string | A unique identifier for the product |
| `soldProducts[].productName` | string | Name of the product |
| `soldProducts[].salesChannel` | string | Where the product was sold (event or store) |
| `soldProducts[].salesChannelReferenceName` | string | Display name of the event or store |
| `soldProducts[].status` | string | Status of the sold product |
| `soldProducts[].storeId` | number | ID of the store if sold through store sales channel |
| `status` | string | Possible states of the order |
| `statusMessage` | string | Message associated with status. |
| `subtotal` | number | Sum without tax |
| `tax` | number | Tax sum |
| `taxTreatment` | string | How tax was calculated |
| `total` | number | Total value of order |
| `totalPaid` | number | Total amount paid for this order including tax |
| `txnId` | string | A unique identifier for the transaction |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/orders` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

