# Bookingmood: Delete Calendar Events

Deletes calendar event records from the Bookingmood API.

```
DELETE https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/delete-calendar-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/delete-calendar-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/delete-calendar-events?${params}`, {
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
      "booking_id": "string",
      "calendar_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "creator_id": "string",
      "duration": 1,
      "end_date": "2026-05-07T12:00:00.000Z",
      "generated_title": "string",
      "has_non_invoiced_items": true,
      "has_open_payments": true,
      "id": "string",
      "notes": "string",
      "occupancy": {},
      "organization_id": "string",
      "origin": "string",
      "padding": 1,
      "product_id": "string",
      "start_date": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "title": "string",
      "type": "string",
      "uid": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `booking_id` | string |  |
| `calendar_id` | string |  |
| `created_at` | date |  |
| `creator_id` | string |  |
| `duration` | number |  |
| `end_date` | date |  |
| `generated_title` | string |  |
| `has_non_invoiced_items` | boolean |  |
| `has_open_payments` | boolean |  |
| `id` | string |  |
| `notes` | string |  |
| `occupancy` | object |  |
| `organization_id` | string |  |
| `origin` | string |  |
| `padding` | number |  |
| `product_id` | string |  |
| `start_date` | date |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `uid` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Bookingmood API, this operation is `DELETE /calendar_events` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-calendar-events.md) for the provider-specific parameters and requirements.

