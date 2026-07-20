# Shipcloud: Create Tracker

Creates a new tracker in Shipcloud.

```
POST https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-tracker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-tracker" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-tracker', {
  method: 'POST',
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
      "carrier": "string",
      "carrier_tracking_no": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "from": {},
      "id": "string",
      "last_polling_at": "2026-05-07T12:00:00.000Z",
      "next_polling_at": "2026-05-07T12:00:00.000Z",
      "shipment_id": "string",
      "status": "string",
      "to": {},
      "tracking_events": [
        {}
      ],
      "tracking_status_updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `carrier_tracking_no` | string |  |
| `created_at` | date |  |
| `from` | object |  |
| `id` | string |  |
| `last_polling_at` | date |  |
| `next_polling_at` | date |  |
| `shipment_id` | string |  |
| `status` | string |  |
| `to` | object |  |
| `tracking_events` | array<object> |  |
| `tracking_status_updated_at` | date |  |

## Native endpoint

Through the native Shipcloud API, this operation is `POST /trackers` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tracker.md) for the provider-specific parameters and requirements.

