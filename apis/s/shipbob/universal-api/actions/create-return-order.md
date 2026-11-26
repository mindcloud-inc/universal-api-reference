# ShipBob: Create Return Order



```
POST https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/create-return-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipBob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/create-return-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fulfillmentCenter": {},
  "fulfillmentCenter.id": 1,
  "inventory[]": [
    {}
  ],
  "inventory[].id": 1,
  "inventory[].quantity": 1,
  "inventory[].requestedAction": "Default",
  "referenceId": "RETURN101"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/create-return-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fulfillmentCenter": {},
    "fulfillmentCenter.id": 1,
    "inventory[]": [{}],
    "inventory[].id": 1,
    "inventory[].quantity": 1,
    "inventory[].requestedAction": "Default",
    "referenceId": "RETURN101"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fulfillmentCenter` | object | yes | The fulfillment center that will process the return. |
| `fulfillmentCenter.id` | list<number> | yes | The ShipBob fulfillment center ID. |
| `inventory[]` | array<object> | yes | The physical inventory items included in this return. |
| `inventory[].id` | list<number> | yes | The ShipBob inventory item ID. |
| `inventory[].quantity` | number | yes | The quantity of this inventory item being returned. |
| `inventory[].requestedAction` | list<string> | yes | How ShipBob should handle the returned item: Default, Restock, Quarantine, or Dispose. One of: `Default`, `Dispose`, `Quarantine`, `Restock`. |
| `referenceId` | string | yes | A unique external reference or RMA number for this return. Example: `RETURN101`. |
| `originalShipmentId` | number | no | The shipment from which the returned items originated. Example: `104458283`. |
| `trackingNumber` | string | no | The tracking number for the return shipment. Example: `1Z9999W99999999999`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inventory[].lotDate` | date | no | The lot date for a lot-tracked inventory item. |
| `inventory[].lotNumber` | string | no | The lot number for a lot-tracked inventory item. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShipBob API returns.

## Native endpoint

Through the native ShipBob API, this operation is `POST 2026-07/return` (base URL `https://{{credentials.apiSubdomain}}.shipbob.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-return-order.md) for the provider-specific parameters and requirements.

