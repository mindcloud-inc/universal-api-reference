# Corsizio: Get Event Details

Retrieves an event from Corsizio by ID.

```
GET https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-event-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Corsizio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-event-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-event-details?${params}`, {
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
| `id` | list<string> | yes | The event ID to request. |
| `include` | list<string> | no | Comma-separated values: filters, stats, attendees, payment. One of: `attendees`, `filters`, `payment`, `stats`. Accepts multiple values in one string, delimited by `,`. |
| `expand` | list<string> | no | Comma-separated values: filters, instructors, account. One of: `account`, `filters`, `instructors`. Accepts multiple values in one string, delimited by `,`. |

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
      "ageGroups": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "attendees": [
        {
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
      "categories": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "contact": {
        "email": "ava@example.com",
        "name": "Ava Chen",
        "phone": "string"
      },
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "descriptionHtml": "string",
      "displayDate": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "formUrl": "https://example.com",
      "genders": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "hideDates": true,
      "id": "string",
      "instructors": [
        [
          "string"
        ]
      ],
      "levels": [
        {
          "id": "string",
          "label": "string"
        }
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
      "stats": {
        "addons": 1,
        "attended": 1,
        "attendees": 1,
        "canceled": 1,
        "certified": 1,
        "discounts": 1,
        "fees": 1,
        "gross": 1,
        "notes": 1,
        "paid": 1,
        "pending": 1,
        "refunds": 1,
        "revenue": 1,
        "soldout": true,
        "spotsNeeded": 1,
        "taxes": 1,
        "total": 1,
        "views": 1,
        "waiting": 1
      },
      "status": "string",
      "summary": "string",
      "summaryHtml": "string",
      "timeZone": "string",
      "videoEmbed": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `account.created` | date |  |
| `account.currency` | string |  |
| `account.id` | string |  |
| `account.name` | string |  |
| `account.siteUrl` | string |  |
| `account.timeZone` | string |  |
| `ageGroups[].id` | string |  |
| `ageGroups[].label` | string |  |
| `attendees[].accountId` | string |  |
| `attendees[].activity[].added` | date |  |
| `attendees[].activity[].author` | string |  |
| `attendees[].activity[].id` | string |  |
| `attendees[].activity[].kind` | string |  |
| `attendees[].activity[].message` | string |  |
| `attendees[].addons[]` | array |  |
| `attendees[].address` | string |  |
| `attendees[].attended` | date |  |
| `attendees[].canceled` | date |  |
| `attendees[].checkin.code` | string |  |
| `attendees[].checkin.entries[]` | array |  |
| `attendees[].checkin.last` | date |  |
| `attendees[].coupon` | object |  |
| `attendees[].created` | date |  |
| `attendees[].email` | string |  |
| `attendees[].eventId` | string |  |
| `attendees[].expunged` | date |  |
| `attendees[].feedback.added` | date |  |
| `attendees[].feedback.asked` | date |  |
| `attendees[].feedback.comment` | string |  |
| `attendees[].feedback.rating` | number |  |
| `attendees[].fields[].label` | string |  |
| `attendees[].fields[].value` | string |  |
| `attendees[].firstName` | string |  |
| `attendees[].id` | string |  |
| `attendees[].lastName` | string |  |
| `attendees[].manual` | boolean |  |
| `attendees[].name` | string |  |
| `attendees[].note` | string |  |
| `attendees[].payment.addons` | number |  |
| `attendees[].payment.amount` | number |  |
| `attendees[].payment.asked` | date |  |
| `attendees[].payment.changed` | date |  |
| `attendees[].payment.currency` | string |  |
| `attendees[].payment.deposit` | boolean |  |
| `attendees[].payment.description` | string |  |
| `attendees[].payment.discount` | number |  |
| `attendees[].payment.discountable` | boolean |  |
| `attendees[].payment.early` | boolean |  |
| `attendees[].payment.exempt` | boolean |  |
| `attendees[].payment.fees` | number |  |
| `attendees[].payment.full` | number |  |
| `attendees[].payment.label` | string |  |
| `attendees[].payment.offline` | boolean |  |
| `attendees[].payment.paid` | date |  |
| `attendees[].payment.pending` | number |  |
| `attendees[].payment.price` | number |  |
| `attendees[].payment.priceId` | string |  |
| `attendees[].payment.refund` | number |  |
| `attendees[].payment.refunded` | boolean |  |
| `attendees[].payment.released` | boolean |  |
| `attendees[].payment.subtotal` | number |  |
| `attendees[].payment.tax` | number |  |
| `attendees[].payment.taxes` | number |  |
| `attendees[].payment.variable` | boolean |  |
| `attendees[].phone` | string |  |
| `attendees[].refCode` | string |  |
| `attendees[].relationToken` | string |  |
| `attendees[].remark` | string |  |
| `attendees[].status` | string |  |
| `attendees[].transactions[].amount` | number |  |
| `attendees[].transactions[].card.brand` | string |  |
| `attendees[].transactions[].card.country` | string |  |
| `attendees[].transactions[].card.last4` | string |  |
| `attendees[].transactions[].card.name` | string |  |
| `attendees[].transactions[].chargeId` | string |  |
| `attendees[].transactions[].created` | date |  |
| `attendees[].transactions[].currency` | string |  |
| `attendees[].transactions[].fees` | number |  |
| `attendees[].transactions[].method` | string |  |
| `attendees[].transactions[].paid` | boolean |  |
| `attendees[].transactions[].refund` | number |  |
| `attendees[].transactions[].refunded` | boolean |  |
| `attendees[].transactions[].refunds[].amount` | number |  |
| `attendees[].transactions[].refunds[].created` | date |  |
| `attendees[].transactions[].refunds[].currency` | string |  |
| `attendees[].transactions[].refunds[].fee` | number |  |
| `attendees[].transactions[].refunds[].id` | string |  |
| `attendees[].transferred` | date |  |
| `attendees[].updated` | date |  |
| `categories[].id` | string |  |
| `categories[].label` | string |  |
| `contact.email` | string |  |
| `contact.name` | string |  |
| `contact.phone` | string |  |
| `created` | date |  |
| `currency` | string |  |
| `descriptionHtml` | string |  |
| `displayDate` | string |  |
| `endDate` | date |  |
| `formUrl` | string |  |
| `genders[].id` | string |  |
| `genders[].label` | string |  |
| `hideDates` | boolean |  |
| `id` | string |  |
| `instructors[]` | array<string> |  |
| `instructors[].bioHtml` | string |  |
| `instructors[].email` | string |  |
| `instructors[].id` | string |  |
| `instructors[].links[].label` | string |  |
| `instructors[].links[].url` | string |  |
| `instructors[].name` | string |  |
| `instructors[].photo` | string |  |
| `instructors[].position` | string |  |
| `levels[].id` | string |  |
| `levels[].label` | string |  |
| `location` | string |  |
| `mapUrl` | string |  |
| `maxSpots` | number |  |
| `name` | string |  |
| `pageUrl` | string |  |
| `photoUrl` | string |  |
| `priceFrom` | number |  |
| `prices[].description` | string |  |
| `prices[].earlyBefore` | date |  |
| `prices[].earlyPrice` | number |  |
| `prices[].label` | string |  |
| `prices[].price` | number |  |
| `priceTo` | number |  |
| `registrationCloseDate` | date |  |
| `startDate` | date |  |
| `stats.addons` | number |  |
| `stats.attended` | number |  |
| `stats.attendees` | number |  |
| `stats.canceled` | number |  |
| `stats.certified` | number |  |
| `stats.discounts` | number |  |
| `stats.fees` | number |  |
| `stats.gross` | number |  |
| `stats.notes` | number |  |
| `stats.paid` | number |  |
| `stats.pending` | number |  |
| `stats.refunds` | number |  |
| `stats.revenue` | number |  |
| `stats.soldout` | boolean |  |
| `stats.spotsNeeded` | number |  |
| `stats.taxes` | number |  |
| `stats.total` | number |  |
| `stats.views` | number |  |
| `stats.waiting` | number |  |
| `status` | string |  |
| `summary` | string |  |
| `summaryHtml` | string |  |
| `timeZone` | string |  |
| `videoEmbed` | string |  |

## Native endpoint

Through the native Corsizio API, this operation is `GET /events/:id` (base URL `https://api.corsizio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-details.md) for the provider-specific parameters and requirements.

