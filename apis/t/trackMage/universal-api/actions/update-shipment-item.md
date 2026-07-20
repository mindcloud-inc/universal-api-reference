# TrackMage: Update Shipment Item

Updates an existing shipment item in TrackMage.

```
PUT https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-shipment-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-shipment-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "orderItem": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-shipment-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "orderItem": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Resource identifier |
| `orderItem` | string | yes | The order item reference to which the shipment items item belongs. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `qty` | number | no | The number of items in the shipment. Default and the minimum value is 0. The value cannot be greater than available quantity of the order item (orderItem.qty - orderItem.fulfilledQty). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalSourceIntegration": "string",
      "externalSourceSyncId": "string",
      "fulfillmentIntegration": "string",
      "fulfillmentSyncId": "string",
      "id": "string",
      "orderItem": "string",
      "qty": 1,
      "shipment": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalSourceIntegration` | string |  |
| `externalSourceSyncId` | string |  |
| `fulfillmentIntegration` | string |  |
| `fulfillmentSyncId` | string |  |
| `id` | string |  |
| `orderItem` | string |  |
| `qty` | number |  |
| `shipment` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `PUT /shipment_items/{id}` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shipment-item.md) for the provider-specific parameters and requirements.

