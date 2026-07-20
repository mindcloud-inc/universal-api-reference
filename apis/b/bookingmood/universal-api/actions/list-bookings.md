# Bookingmood: List Bookings

Retrieves booking records from the Bookingmood API.

```
GET https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-bookings?${params}`, {
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
      "confirmed_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "creator_id": "string",
      "currency": "string",
      "display_currency": "string",
      "exchange_rate": 1,
      "id": "string",
      "method": "string",
      "organization_id": "string",
      "reference": "string",
      "secret": "string",
      "silent": true,
      "site_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "widget_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmed_at` | date |  |
| `created_at` | date |  |
| `creator_id` | string |  |
| `currency` | string |  |
| `display_currency` | string |  |
| `exchange_rate` | number |  |
| `id` | string |  |
| `method` | string |  |
| `organization_id` | string |  |
| `reference` | string |  |
| `secret` | string |  |
| `silent` | boolean |  |
| `site_id` | string |  |
| `updated_at` | date |  |
| `widget_id` | string |  |

## Native endpoint

Through the native Bookingmood API, this operation is `GET /bookings` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

