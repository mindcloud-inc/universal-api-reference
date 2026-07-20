# Starshipit: Print Label



```
POST https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/print-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/print-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/print-label', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | no |  |
| `carrier` | string | no |  |
| `carrierServiceCode` | string | no |  |
| `packages[]` | array<object> | no |  |
| `reprint` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationjson": {
        "carrierName": "Ava Chen",
        "labels": [
          "string"
        ],
        "labelTypes": [
          "string"
        ],
        "orderId": 1,
        "orderNumber": "string",
        "success": true,
        "trackingNumbers": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationjson` | object |  |
| `applicationjson.carrierName` | string |  |
| `applicationjson.labels` | array<string> |  |
| `applicationjson.labelTypes` | array<string> |  |
| `applicationjson.orderId` | number |  |
| `applicationjson.orderNumber` | string |  |
| `applicationjson.success` | boolean |  |
| `applicationjson.trackingNumbers` | array<string> |  |

## Native endpoint

Through the native Starshipit API, this operation is `POST /orders/shipment` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/print-label.md) for the provider-specific parameters and requirements.

