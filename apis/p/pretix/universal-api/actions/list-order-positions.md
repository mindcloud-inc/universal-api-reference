# pretix: List Order Positions

Retrieves order positions from a pretix event.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-order-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-order-positions?connectionId=$CONNECTION_ID&limit=25&offset=0&organizer=string&event=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-order-positions?${params}`, {
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
| `order` | string | no | Optional order code filter for order positions. |
| `organizer` | string | yes | pretix organizer slug. |
| `event` | string | yes | pretix event slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendeeEmail": "ava@example.com",
      "attendeeName": "Ava Chen",
      "canceled": true,
      "city": "string",
      "company": "string",
      "country": "string",
      "id": 1,
      "item": 1,
      "order": "string",
      "positionid": 1,
      "price": "string",
      "state": "string",
      "street": "string",
      "variation": 1,
      "voucher": 1,
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendeeEmail` | string |  |
| `attendeeName` | string |  |
| `canceled` | boolean |  |
| `city` | string |  |
| `company` | string |  |
| `country` | string |  |
| `id` | number |  |
| `item` | number |  |
| `order` | string |  |
| `positionid` | number |  |
| `price` | string |  |
| `state` | string |  |
| `street` | string |  |
| `variation` | number |  |
| `voucher` | number |  |
| `zipcode` | string |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/orderpositions/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-order-positions.md) for the provider-specific parameters and requirements.

