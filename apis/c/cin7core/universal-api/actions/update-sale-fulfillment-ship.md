# Cin7 Core: Update Sale Fulfillment Ship



```
PUT https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/update-sale-fulfillment-ship
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cin7 Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/update-sale-fulfillment-ship" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "TaskID": "string",
  "Status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/update-sale-fulfillment-ship', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "TaskID": "string",
    "Status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Lines[].ShipmentDate` | string | no |  |
| `ShippingAddress.DisplayAddressLine1` | string | no |  |
| `TaskID` | string | yes |  |
| `Lines[].Carrier` | string | no |  |
| `ShippingAddress.DisplayAddressLine2` | string | no |  |
| `Status` | string | yes |  |
| `Lines[].Box` | string | no |  |
| `RequireBy` | string | no |  |
| `ShippingAddress.Line1` | string | no |  |
| `Lines[].TrackingNumber` | string | no |  |
| `ShippingAddress` | object | no |  |
| `ShippingAddress.Line2` | string | no |  |
| `Lines[].TrackingURL` | string | no |  |
| `ShippingAddress.City` | string | no |  |
| `ShippingNotes` | string | no |  |
| `Lines[]` | array<object> | no |  |
| `Lines[].IsShipped` | boolean | no |  |
| `ShippingAddress.State` | string | no |  |
| `ShippingAddress.Postcode` | string | no |  |
| `ShippingAddress.Country` | string | no |  |
| `ShippingAddress.Company` | string | no |  |
| `ShippingAddress.Contact` | string | no |  |
| `ShippingAddress.ShipToOther` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cin7 Core API returns.

## Native endpoint

Through the native Cin7 Core API, this operation is `PUT sale/fulfilment/ship` (base URL `https://inventory.dearsystems.com/externalapi/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sale-fulfillment-ship.md) for the provider-specific parameters and requirements.

