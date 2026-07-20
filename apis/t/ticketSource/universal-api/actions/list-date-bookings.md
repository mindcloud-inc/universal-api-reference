# TicketSource: List Date Bookings

Retrieves bookings for a date from TicketSource.

```
GET https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-date-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TicketSource `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-date-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0&dateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "dateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-date-bookings?${params}`, {
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
| `dateId` | string | yes | The unique identifier for a Date record |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "consent": {
          "email": true,
          "post": true,
          "sms": true,
          "thirdParty": "string"
        },
        "createdAt": "2026-05-07T12:00:00.000Z",
        "lines": [
          {
            "amount": {
              "discounts": {
                "automatic": 1,
                "code": {
                  "amount": 1,
                  "description": "string"
                }
              },
              "fee": 1,
              "feeVat": 1,
              "gross": 1,
              "net": 1
            },
            "createdAt": "2026-05-07T12:00:00.000Z",
            "donation": {
              "giftAid": true
            },
            "isRefund": true,
            "lineType": "string",
            "paymentMethod": "string",
            "updatedAt": "2026-05-07T12:00:00.000Z"
          }
        ],
        "ref": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "userBookedBy": "string"
      },
      "id": "string",
      "links": {
        "customer": "https://example.com",
        "date": "https://example.com",
        "seats": "https://example.com",
        "self": "https://example.com"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.consent.email` | boolean |  |
| `attributes.consent.post` | boolean |  |
| `attributes.consent.sms` | boolean |  |
| `attributes.consent.thirdParty` | string |  |
| `attributes.createdAt` | date |  |
| `attributes.lines[].amount.discounts.automatic` | number |  |
| `attributes.lines[].amount.discounts.code.amount` | number |  |
| `attributes.lines[].amount.discounts.code.description` | string |  |
| `attributes.lines[].amount.fee` | number |  |
| `attributes.lines[].amount.feeVat` | number |  |
| `attributes.lines[].amount.gross` | number |  |
| `attributes.lines[].amount.net` | number |  |
| `attributes.lines[].createdAt` | date |  |
| `attributes.lines[].donation.giftAid` | boolean |  |
| `attributes.lines[].isRefund` | boolean |  |
| `attributes.lines[].lineType` | string |  |
| `attributes.lines[].paymentMethod` | string |  |
| `attributes.lines[].updatedAt` | date |  |
| `attributes.ref` | string |  |
| `attributes.updatedAt` | date |  |
| `attributes.userBookedBy` | string |  |
| `id` | string |  |
| `links.customer` | string |  |
| `links.date` | string |  |
| `links.seats` | string |  |
| `links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native TicketSource API, this operation is `GET /dates/{DateId}/bookings` (base URL `https://api.ticketsource.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-date-bookings.md) for the provider-specific parameters and requirements.

