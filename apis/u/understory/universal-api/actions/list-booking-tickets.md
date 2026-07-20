# Understory: List Booking Tickets

Retrieves tickets for a booking in Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-booking-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-booking-tickets?connectionId=$CONNECTION_ID&bookingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-booking-tickets?${params}`, {
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
| `bookingId` | string | yes | The unique identifier of the booking. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "check_in": {
            "check_in_time": "2026-05-07T12:00:00.000Z",
            "checked_in_by": "string",
            "method": "string"
          },
          "id": "string",
          "items": [
            {
              "item_type": "string",
              "quantity": 1,
              "type_id": "string"
            }
          ],
          "status": "string",
          "urls": [
            {
              "type": "https://example.com",
              "url": "https://example.com"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].check_in.check_in_time` | date |  |
| `items[].check_in.checked_in_by` | string |  |
| `items[].check_in.method` | string |  |
| `items[].id` | string |  |
| `items[].items[].item_type` | string |  |
| `items[].items[].quantity` | number |  |
| `items[].items[].type_id` | string |  |
| `items[].status` | string |  |
| `items[].urls[].type` | string |  |
| `items[].urls[].url` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/bookings/{{bookingId}}/tickets` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-booking-tickets.md) for the provider-specific parameters and requirements.

