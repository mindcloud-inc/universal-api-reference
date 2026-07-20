# pretix: Get Order

Retrieves an order from pretix.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-order?connectionId=$CONNECTION_ID&organizer=string&event=string&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizer": "string",
  "event": "string",
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-order?${params}`, {
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
| `organizer` | string | yes | pretix organizer slug. |
| `event` | string | yes | pretix event slug. |
| `code` | string | yes | pretix order code. |

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

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/orders/:code/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

