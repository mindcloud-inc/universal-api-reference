# pretix: List Orders

Retrieves orders from a pretix event.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&organizer=string&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizer": "string",
  "event": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-orders?${params}`, {
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
| `email` | string | no | Only return orders created with this email address. |
| `organizer` | string | yes | pretix organizer slug. |
| `search` | string | no | Search query for matching order names, emails, or companies. |
| `event` | string | yes | pretix event slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkinAttention": true,
      "code": "string",
      "comment": "string",
      "customer": "string",
      "datetime": "string",
      "email": "ava@example.com",
      "event": "string",
      "expires": "string",
      "invoiceAddress": {},
      "locale": "string",
      "phone": "string",
      "salesChannel": "string",
      "status": "string",
      "testmode": true,
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkinAttention` | boolean |  |
| `code` | string |  |
| `comment` | string |  |
| `customer` | string |  |
| `datetime` | string |  |
| `email` | string |  |
| `event` | string |  |
| `expires` | string |  |
| `invoiceAddress` | object |  |
| `locale` | string |  |
| `phone` | string |  |
| `salesChannel` | string |  |
| `status` | string |  |
| `testmode` | boolean |  |
| `total` | string |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/orders/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

