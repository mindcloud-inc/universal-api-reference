# ShipBob: Edit Return Order



```
PUT https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/edit-return-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipBob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/edit-return-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "123456",
  "fulfillmentCenter": {},
  "fulfillmentCenter.id": 1,
  "inventory[]": [
    {}
  ],
  "inventory[].id": 1,
  "inventory[].quantity": "1",
  "inventory[].requestedAction": "0",
  "referenceId": "RETURN101"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/edit-return-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "123456",
    "fulfillmentCenter": {},
    "fulfillmentCenter.id": 1,
    "inventory[]": [{}],
    "inventory[].id": 1,
    "inventory[].quantity": "1",
    "inventory[].requestedAction": "0",
    "referenceId": "RETURN101"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ShipBob return order ID to edit. Example: `123456`. |
| `fulfillmentCenter` | object | yes | The fulfillment center receiving the return. |
| `fulfillmentCenter.id` | list<number> | yes | The ShipBob fulfillment center that will receive the return. |
| `inventory[]` | array<object> | yes | The returned inventory items and requested handling actions. |
| `inventory[].id` | list<number> | yes | The ShipBob inventory item being returned. |
| `inventory[].quantity` | number | yes | The quantity of this inventory item being returned. Example: `1`. |
| `inventory[].requestedAction` | list | yes | How ShipBob should handle this returned inventory item. One of: `0`, `1`, `2`, `3`. |
| `referenceId` | string | yes | Your unique reference for this return order. Example: `RETURN101`. |
| `originalShipmentId` | number | no | The original ShipBob shipment ID, when available. Example: `104458283`. |
| `trackingNumber` | string | no | The carrier tracking number for the return package. Example: `1Z999AA10123456784`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inventory[].lotDate` | date | no | The lot date for this inventory item, when applicable. |
| `inventory[].lotNumber` | string | no | The lot number for this inventory item, when applicable. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShipBob API returns.

## Native endpoint

Through the native ShipBob API, this operation is `PUT 2026-07/return/:id` (base URL `https://{{credentials.apiSubdomain}}.shipbob.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-return-order.md) for the provider-specific parameters and requirements.

