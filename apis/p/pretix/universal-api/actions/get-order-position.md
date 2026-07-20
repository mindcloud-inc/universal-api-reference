# pretix: Get Order Position

Retrieves an order position from pretix.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-order-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-order-position?connectionId=$CONNECTION_ID&organizer=string&event=string&position=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizer": "string",
  "event": "string",
  "position": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-order-position?${params}`, {
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
| `position` | string | yes | pretix order position ID. |

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

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/orderpositions/:position/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-position.md) for the provider-specific parameters and requirements.

