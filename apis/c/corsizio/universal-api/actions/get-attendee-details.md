# Corsizio: Get Attendee Details

Retrieves an attendee from Corsizio by ID.

```
GET https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-attendee-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Corsizio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-attendee-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-attendee-details?${params}`, {
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
| `id` | list<string> | yes | The attendee ID to request. |
| `include` | list<string> | no | Comma-separated values: payment, activity, details. One of: `activity`, `details`, `payment`. Accepts multiple values in one string, delimited by `,`. |
| `expand` | list<string> | no | Comma-separated values: event, account. One of: `account`, `event`. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "created": "2026-05-07T12:00:00.000Z",
        "currency": "string",
        "id": "string",
        "name": "Ava Chen",
        "siteUrl": "https://example.com",
        "timeZone": "string"
      },
      "accountId": "string",
      "activity": [
        {
          "added": "2026-05-07T12:00:00.000Z",
          "author": "string",
          "id": "string",
          "kind": "string",
          "message": "string"
        }
      ],
      "addons": [
        [
          "string"
        ]
      ],
      "address": "string",
      "attended": "2026-05-07T12:00:00.000Z",
      "canceled": "2026-05-07T12:00:00.000Z",
      "checkin": {
        "code": "string",
        "entries": [
          [
            "string"
          ]
        ],
        "last": "2026-05-07T12:00:00.000Z"
      },
      "coupon": {},
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "event": {
        "account": {
          "created": "2026-05-07T12:00:00.000Z",
          "currency": "string",
          "id": "string",
          "name": "Ava Chen",
          "siteUrl": "https://example.com",
          "timeZone": "string"
        },
        "contact": {
          "email": "ava@example.com",
          "name": "Ava Chen"
        },
        "created": "2026-05-07T12:00:00.000Z",
        "currency": "string",
        "descriptionHtml": "string",
        "displayDate": "string",
        "endDate": "2026-05-07T12:00:00.000Z",
        "formUrl": "https://example.com",
        "id": "string",
        "instructors": [
          [
            "string"
          ]
        ],
        "location": "string",
        "mapUrl": "https://example.com",
        "maxSpots": 1,
        "name": "Ava Chen",
        "pageUrl": "https://example.com",
        "photoUrl": "https://example.com",
        "priceFrom": 1,
        "prices": [
          {
            "description": "string",
            "earlyBefore": "2026-05-07T12:00:00.000Z",
            "earlyPrice": 1,
            "label": "string",
            "price": 1
          }
        ],
        "priceTo": 1,
        "registrationCloseDate": "2026-05-07T12:00:00.000Z",
        "startDate": "2026-05-07T12:00:00.000Z",
        "status": "string",
        "summary": "string",
        "summaryHtml": "string",
        "timeZone": "string",
        "videoEmbed": "string"
      },
      "eventId": "string",
      "expunged": "2026-05-07T12:00:00.000Z",
      "feedback": {
        "added": "2026-05-07T12:00:00.000Z",
        "asked": "2026-05-07T12:00:00.000Z",
        "comment": "string",
        "rating": 1
      },
      "fields": [
        {
          "label": "string",
          "value": "string"
        }
      ],
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "manual": true,
      "name": "Ava Chen",
      "note": "string",
      "payment": {
        "addons": 1,
        "amount": 1,
        "asked": "2026-05-07T12:00:00.000Z",
        "changed": "2026-05-07T12:00:00.000Z",
        "currency": "string",
        "deposit": true,
        "description": "string",
        "discount": 1,
        "discountable": true,
        "early": true,
        "exempt": true,
        "fees": 1,
        "full": 1,
        "label": "string",
        "offline": true,
        "paid": "2026-05-07T12:00:00.000Z",
        "pending": 1,
        "price": 1,
        "priceId": "string",
        "refund": 1,
        "refunded": true,
        "released": true,
        "subtotal": 1,
        "tax": 1,
        "taxes": 1,
        "variable": true
      },
      "phone": "string",
      "refCode": "string",
      "relationToken": "string",
      "remark": "string",
      "status": "string",
      "transactions": [
        {
          "amount": 1,
          "card": {
            "brand": "string",
            "country": "string",
            "last4": "string",
            "name": "Ava Chen"
          },
          "chargeId": "string",
          "created": "2026-05-07T12:00:00.000Z",
          "currency": "string",
          "fees": 1,
          "method": "string",
          "paid": true,
          "refund": 1,
          "refunded": true,
          "refunds": [
            {
              "amount": 1,
              "created": "2026-05-07T12:00:00.000Z",
              "currency": "string",
              "fee": 1,
              "id": "string"
            }
          ]
        }
      ],
      "transferred": "2026-05-07T12:00:00.000Z",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.created` | date |  |
| `account.currency` | string |  |
| `account.id` | string |  |
| `account.name` | string |  |
| `account.siteUrl` | string |  |
| `account.timeZone` | string |  |
| `accountId` | string |  |
| `activity[].added` | date |  |
| `activity[].author` | string |  |
| `activity[].id` | string |  |
| `activity[].kind` | string |  |
| `activity[].message` | string |  |
| `addons[]` | array |  |
| `address` | string |  |
| `attended` | date |  |
| `canceled` | date |  |
| `checkin.code` | string |  |
| `checkin.entries[]` | array |  |
| `checkin.last` | date |  |
| `coupon` | object |  |
| `created` | date |  |
| `email` | string |  |
| `event.account.created` | date |  |
| `event.account.currency` | string |  |
| `event.account.id` | string |  |
| `event.account.name` | string |  |
| `event.account.siteUrl` | string |  |
| `event.account.timeZone` | string |  |
| `event.contact.email` | string |  |
| `event.contact.name` | string |  |
| `event.created` | date |  |
| `event.currency` | string |  |
| `event.descriptionHtml` | string |  |
| `event.displayDate` | string |  |
| `event.endDate` | date |  |
| `event.formUrl` | string |  |
| `event.id` | string |  |
| `event.instructors[]` | array<string> |  |
| `event.location` | string |  |
| `event.mapUrl` | string |  |
| `event.maxSpots` | number |  |
| `event.name` | string |  |
| `event.pageUrl` | string |  |
| `event.photoUrl` | string |  |
| `event.priceFrom` | number |  |
| `event.prices[].description` | string |  |
| `event.prices[].earlyBefore` | date |  |
| `event.prices[].earlyPrice` | number |  |
| `event.prices[].label` | string |  |
| `event.prices[].price` | number |  |
| `event.priceTo` | number |  |
| `event.registrationCloseDate` | date |  |
| `event.startDate` | date |  |
| `event.status` | string |  |
| `event.summary` | string |  |
| `event.summaryHtml` | string |  |
| `event.timeZone` | string |  |
| `event.videoEmbed` | string |  |
| `eventId` | string |  |
| `expunged` | date |  |
| `feedback.added` | date |  |
| `feedback.asked` | date |  |
| `feedback.comment` | string |  |
| `feedback.rating` | number |  |
| `fields[].label` | string |  |
| `fields[].value` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `manual` | boolean |  |
| `name` | string |  |
| `note` | string |  |
| `payment.addons` | number |  |
| `payment.amount` | number |  |
| `payment.asked` | date |  |
| `payment.changed` | date |  |
| `payment.currency` | string |  |
| `payment.deposit` | boolean |  |
| `payment.description` | string |  |
| `payment.discount` | number |  |
| `payment.discountable` | boolean |  |
| `payment.early` | boolean |  |
| `payment.exempt` | boolean |  |
| `payment.fees` | number |  |
| `payment.full` | number |  |
| `payment.label` | string |  |
| `payment.offline` | boolean |  |
| `payment.paid` | date |  |
| `payment.pending` | number |  |
| `payment.price` | number |  |
| `payment.priceId` | string |  |
| `payment.refund` | number |  |
| `payment.refunded` | boolean |  |
| `payment.released` | boolean |  |
| `payment.subtotal` | number |  |
| `payment.tax` | number |  |
| `payment.taxes` | number |  |
| `payment.variable` | boolean |  |
| `phone` | string |  |
| `refCode` | string |  |
| `relationToken` | string |  |
| `remark` | string |  |
| `status` | string |  |
| `transactions[].amount` | number |  |
| `transactions[].card.brand` | string |  |
| `transactions[].card.country` | string |  |
| `transactions[].card.last4` | string |  |
| `transactions[].card.name` | string |  |
| `transactions[].chargeId` | string |  |
| `transactions[].created` | date |  |
| `transactions[].currency` | string |  |
| `transactions[].fees` | number |  |
| `transactions[].method` | string |  |
| `transactions[].paid` | boolean |  |
| `transactions[].refund` | number |  |
| `transactions[].refunded` | boolean |  |
| `transactions[].refunds[].amount` | number |  |
| `transactions[].refunds[].created` | date |  |
| `transactions[].refunds[].currency` | string |  |
| `transactions[].refunds[].fee` | number |  |
| `transactions[].refunds[].id` | string |  |
| `transferred` | date |  |
| `updated` | date |  |

## Native endpoint

Through the native Corsizio API, this operation is `GET /attendees/:id` (base URL `https://api.corsizio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attendee-details.md) for the provider-specific parameters and requirements.

