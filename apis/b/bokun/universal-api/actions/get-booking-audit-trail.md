# Bokun: Get Booking Audit Trail

Retrieves audit trail records for a booking from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-booking-audit-trail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-booking-audit-trail?connectionId=$CONNECTION_ID&bookingId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookingId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-booking-audit-trail?${params}`, {
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
| `bookingId` | number | yes | The Bokun booking ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "bookingChannelId": 1,
      "bookingId": 1,
      "date": 1,
      "errorOccurred": true,
      "extranetUsername": "Ava Chen",
      "id": 1,
      "location": "string",
      "productBookingId": 1,
      "referer": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `bookingChannelId` | number |  |
| `bookingId` | number |  |
| `date` | number |  |
| `errorOccurred` | boolean |  |
| `extranetUsername` | string |  |
| `id` | number |  |
| `location` | string |  |
| `productBookingId` | number |  |
| `referer` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/booking/:bookingId/audit-records` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking-audit-trail.md) for the provider-specific parameters and requirements.

