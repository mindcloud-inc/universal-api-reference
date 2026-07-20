# Restoplace: Update Booking Item

Updates an existing booking item in Restoplace.

```
PUT https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/update-booking-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restoplace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/update-booking-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/update-booking-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique Restoplace booking item ID. |
| `type` | string | no | Booking item type from the List Item Types action. |
| `floorId` | number | no | Hall ID that owns the booking item. |
| `number` | string | no | Visible item number. |
| `countMin` | number | no | Minimum guest capacity. |
| `countMax` | number | no | Maximum guest capacity. |
| `text` | string | no | Booking item description or comment. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checked` | number | no | Whether the booking item is enabled. |
| `reserve` | number | no | Whether guests can book the item through the widget. |
| `groupReserve` | number | no | Whether the item is available for group reservations. |
| `viewOnlyHostess` | number | no | Whether the item is visible only to staff. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restoplace API returns.

## Native endpoint

Through the native Restoplace API, this operation is `PUT /items/:id` (base URL `https://api.restoplace.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-booking-item.md) for the provider-specific parameters and requirements.

