# DateX: Update Shipment Markup Cost



```
PUT https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/update-shipment-markup-cost
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/update-shipment-markup-cost" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "update.customerFreight": "12.5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/update-shipment-markup-cost', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "update.customerFreight": "12.5"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters.orderId` | string | no | Order ID filter used to find the shipment. |
| `filters.orderLookup` | string | no | Order lookup filter used to find the shipment. |
| `filters.shipmentId` | string | no | Shipment ID filter used to find the shipment. |
| `filters.shipmentLookup` | string | no | Shipment lookup filter used to find the shipment. |
| `update.customerFreight` | number | yes | New customer freight markup cost. Example: `12.5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shipmentId": "string",
      "update": {
        "customerFreight": {
          "from": 1,
          "to": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shipmentId` | string |  |
| `update.customerFreight.from` | number |  |
| `update.customerFreight.to` | number |  |

## Native endpoint

Through the native DateX API, this operation is `POST shipment/update` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shipment-markup-cost.md) for the provider-specific parameters and requirements.

