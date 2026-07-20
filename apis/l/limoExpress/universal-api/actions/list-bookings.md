# LimoExpress: List Bookings

Retrieves bookings from the LimoExpress organization.

```
GET https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-bookings?${params}`, {
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
| `pickupDateFrom` | string | no | Filter bookings with pickup time from this datetime. |
| `pickupDateTo` | string | no | Filter bookings with pickup time to this datetime. |
| `paymentMethodId` | string | no | Filter by payment method identifier. |
| `bookingTypeId` | string | no | Filter by booking type identifier. |
| `bookingStatusId` | number | no | Filter by booking status identifier. |
| `vehicleId` | string | no | Filter by vehicle identifier. |
| `clientId` | string | no | Filter by client identifier. |
| `searchString` | string | no | Search value across booking fields. |
| `order` | string | no | Sort direction. Allowed values: asc or desc. |
| `orderBy` | string | no | Sort field. Available values include pickup_time and id. |
| `page` | number | no | Page number, default is 1. |
| `perPage` | number | no | Items per page, default is 20. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "links": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Booking rows. |
| `links` | object | Pagination links. |
| `meta` | object | Pagination metadata. |

## Native endpoint

Through the native LimoExpress API, this operation is `GET /api/integration/bookings` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

