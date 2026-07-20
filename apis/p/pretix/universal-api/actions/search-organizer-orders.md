# pretix: Search Organizer Orders

Searches orders across a pretix organizer.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/search-organizer-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/search-organizer-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&organizer=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizer": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/search-organizer-orders?${params}`, {
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
| `search` | string | no | Search query for matching order names, emails, or companies. |

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

Through the native pretix API, this operation is `GET /organizers/:organizer/orders/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-organizer-orders.md) for the provider-specific parameters and requirements.

