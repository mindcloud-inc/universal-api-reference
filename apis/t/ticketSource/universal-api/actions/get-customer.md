# TicketSource: Get Customer

Retrieves a customer from the TicketSource account.

```
GET https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TicketSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-customer?${params}`, {
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
| `customerId` | string | yes | The unique identifier for a Customer record |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "address": {
          "line1": "string",
          "line2": "string",
          "line3": "string",
          "line4": "string",
          "postcode": "string"
        },
        "consent": {
          "email": true,
          "post": true,
          "sms": true
        },
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "membership": {
          "endDate": "2026-05-07T12:00:00.000Z",
          "identifier": "string",
          "startDate": "2026-05-07T12:00:00.000Z"
        },
        "phone": "string",
        "telephone": "string",
        "title": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "links": {
        "bookings": "https://example.com",
        "notes": "https://example.com",
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
| `attributes.address.line1` | string |  |
| `attributes.address.line2` | string |  |
| `attributes.address.line3` | string |  |
| `attributes.address.line4` | string |  |
| `attributes.address.postcode` | string |  |
| `attributes.consent.email` | boolean |  |
| `attributes.consent.post` | boolean |  |
| `attributes.consent.sms` | boolean |  |
| `attributes.createdAt` | date |  |
| `attributes.email` | string |  |
| `attributes.firstName` | string |  |
| `attributes.lastName` | string |  |
| `attributes.membership.endDate` | date |  |
| `attributes.membership.identifier` | string |  |
| `attributes.membership.startDate` | date |  |
| `attributes.phone` | string | See 'telephone' |
| `attributes.telephone` | string |  |
| `attributes.title` | string | No longer in use in the TicketSource system. |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `links.bookings` | string |  |
| `links.notes` | string |  |
| `links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native TicketSource API, this operation is `GET /customers/{CustomerId}` (base URL `https://api.ticketsource.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

