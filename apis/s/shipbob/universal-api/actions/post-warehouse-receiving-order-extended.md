# ShipBob: Post Warehouse Receiving Order (Extended)



```
POST https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/post-warehouse-receiving-order-extended
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipBob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/post-warehouse-receiving-order-extended" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/post-warehouse-receiving-order-extended', {
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
| `fulfillmentCenter.id` | number | no |  |
| `boxes[].boxItems[].quantity` | string | no |  |
| `boxes[].trackingNumber` | string | no |  |
| `fulfillmentCenter` | object | no |  |
| `tags[].name` | string | no |  |
| `boxes[].boxItems[]` | array | no |  |
| `boxes[].boxItems[].inventoryId` | string | no |  |
| `packageType` | list | no |  |
| `tags[].value` | string | no |  |
| `boxes[].boxItems[].lot_number` | string | no |  |
| `boxPackagingType` | list | no |  |
| `purchaseOrderNumber` | string | no |  |
| `expectedArrivalDate` | string | no |  |
| `boxes[]` | array | no |  |
| `fulfillmentCentere.id` | string | no |  |
| `fullasdfasdf.id` | string | no |  |
| `tags[]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShipBob API returns.

## Native endpoint

Through the native ShipBob API, this operation is `POST 2.0/receiving-extended` (base URL `https://{{credentials.apiSubdomain}}.shipbob.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-warehouse-receiving-order-extended.md) for the provider-specific parameters and requirements.

