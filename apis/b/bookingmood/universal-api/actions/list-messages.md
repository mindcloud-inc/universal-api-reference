# Bookingmood: List Messages

Retrieves messages scheduled or sent to Bookingmood guests.

```
GET https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-messages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "body": "string",
      "booking_id": "string",
      "calendar_event_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "html": "string",
      "id": "string",
      "include_booking_details": true,
      "include_booking_link": true,
      "include_ical_data": true,
      "include_product_image": true,
      "message_template_id": "string",
      "send_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subject": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `body` | string |  |
| `booking_id` | string |  |
| `calendar_event_id` | string |  |
| `created_at` | date |  |
| `html` | string |  |
| `id` | string |  |
| `include_booking_details` | boolean |  |
| `include_booking_link` | boolean |  |
| `include_ical_data` | boolean |  |
| `include_product_image` | boolean |  |
| `message_template_id` | string |  |
| `send_at` | date |  |
| `status` | string |  |
| `subject` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Bookingmood API, this operation is `GET /messages` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

