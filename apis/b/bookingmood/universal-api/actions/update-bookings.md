# Bookingmood: Update Bookings

Updates booking records in the Bookingmood API.

```
PUT https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/update-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/update-bookings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/update-bookings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Bookingmood API, this operation is `PATCH /bookings` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bookings.md) for the provider-specific parameters and requirements.

