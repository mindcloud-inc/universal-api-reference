# Beds24: List Booking.com Reviews

Retrieves Booking.com reviews from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-booking-com-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-booking-com-reviews?connectionId=$CONNECTION_ID&from=string&propertyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "propertyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-booking-com-reviews?${params}`, {
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
| `from` | string | yes | Lower bound timestamp or date for Booking.com reviews. |
| `propertyId` | number | yes | Beds24 property ID whose Booking.com reviews should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "created_timestamp": "2026-05-07T12:00:00.000Z",
      "reservation_id": "string",
      "review_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object | Review content object. |
| `created_timestamp` | date | Review creation timestamp. |
| `reservation_id` | string | Associated reservation identifier. |
| `review_id` | string | Booking.com review identifier. |

## Native endpoint

Through the native Beds24 API, this operation is `GET /channels/booking/reviews` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-booking-com-reviews.md) for the provider-specific parameters and requirements.

