# Shipcloud: Create Shipment

Creates a new shipment in Shipcloud.

```
POST https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-shipment', {
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
      "carrier_tracking_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "customs_declaration": {},
      "from": {},
      "id": "string",
      "label_url": "https://example.com",
      "packages": [
        {}
      ],
      "price": 1,
      "reference_number": "string",
      "service": "string",
      "shipper_notification_email": "ava@example.com",
      "to": {},
      "tracking_url": "https://example.com"
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
| `carrier_tracking_url` | string |  |
| `created_at` | date |  |
| `customs_declaration` | object |  |
| `from` | object |  |
| `id` | string |  |
| `label_url` | string |  |
| `packages` | array<object> |  |
| `price` | number |  |
| `reference_number` | string |  |
| `service` | string |  |
| `shipper_notification_email` | string |  |
| `to` | object |  |
| `tracking_url` | string |  |

## Native endpoint

Through the native Shipcloud API, this operation is `POST /shipments` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment.md) for the provider-specific parameters and requirements.

