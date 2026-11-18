# Brightpearl: Create Goods-In Note



```
POST https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-goods-in-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-goods-in-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-goods-in-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | yes |  |
| `warehouseId` | number | no |  |
| `goodsMoved[]` | array<object> | no |  |
| `goodsMoved[].productId` | number | no |  |
| `goodsMoved[].purchaseOrderRowId` | number | no |  |
| `goodsMoved[].quantity` | number | no |  |
| `goodsMoved[].destinationLocationId` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `goodsMoved[].productValue` | object | no |  |
| `goodsMoved[].productValue.currency` | string | no |  |
| `goodsMoved[].productValue.value` | number | no |  |
| `transfer` | boolean | no |  |
| `receivedOn` | date | no |  |
| `userBatchReference` | string | no | Optional reference that must be unique across goods-in notes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Brightpearl API, this operation is `POST /warehouse-service/order/:orderId/goods-note/goods-in` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-goods-in-note.md) for the provider-specific parameters and requirements.

