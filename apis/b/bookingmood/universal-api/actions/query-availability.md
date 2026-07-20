# Bookingmood: Query Availability

Retrieves long-range availability for multiple Bookingmood products.

```
GET https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/query-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/query-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/query-availability?${params}`, {
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
| `performSync` | boolean | no | Whether to sync external calendars before fetching availability. |
| `productId` | string | no | Product ID to fetch availability for. |
| `showBookedAs` | string | no | How to interpret confirmed bookings. |
| `showClosedAs` | string | no | How to interpret blocked or closed periods. |
| `showPendingAs` | string | no | How to interpret pending events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "intervals": [
        {}
      ],
      "product_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `intervals` | array<object> |  |
| `product_id` | string |  |

## Native endpoint

Through the native Bookingmood API, this operation is `GET /availability` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-availability.md) for the provider-specific parameters and requirements.

