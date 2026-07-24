# Cin7 Core: Create Sale Fulfillment Ship



```
POST https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/create-sale-fulfillment-ship
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cin7 Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/create-sale-fulfillment-ship" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "status": "string",
  "taskID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/create-sale-fulfillment-ship', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "status": "string",
    "taskID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lines[].ShipmentDate` | date | no |  |
| `shippingAddress.DisplayAddressLine1` | string | no |  |
| `lines[].Carrier` | string | no |  |
| `shippingAddress.DisplayAddressLine2` | string | no |  |
| `lines[].Box` | string | no |  |
| `shippingAddress.Line1` | string | no |  |
| `lines[].TrackingNumber` | string | no |  |
| `shippingAddress.Line2` | string | no |  |
| `lines[].TrackingURL` | string | no |  |
| `shippingAddress.City` | string | no |  |
| `lines[].IsShipped` | boolean | no |  |
| `shippingAddress.State` | string | no |  |
| `shippingAddress.Postcode` | string | no |  |
| `shippingAddress.Country` | string | no |  |
| `shippingAddress.Company` | string | no |  |
| `shippingAddress.Contact` | string | no |  |
| `shippingAddress.ShipToOther` | boolean | no |  |
| `lines[]` | array<object> | no |  |
| `requireBy` | string | no |  |
| `shippingAddress` | object | no |  |
| `shippingNotes` | string | no |  |
| `status` | string | yes |  |
| `taskID` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cin7 Core API returns.

## Native endpoint

Through the native Cin7 Core API, this operation is `POST sale/fulfilment/ship` (base URL `https://inventory.dearsystems.com/externalapi/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sale-fulfillment-ship.md) for the provider-specific parameters and requirements.

