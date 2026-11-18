# Brightpearl: Create Stock Corrections



```
POST https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-stock-corrections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-stock-corrections" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "warehouseId": 1,
  "corrections[]": [
    {}
  ],
  "corrections[].quantity": 1,
  "corrections[].productId": 1,
  "corrections[].reason": "string",
  "corrections[].locationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-stock-corrections', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "warehouseId": 1,
    "corrections[]": [{}],
    "corrections[].quantity": 1,
    "corrections[].productId": 1,
    "corrections[].reason": "string",
    "corrections[].locationId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `warehouseId` | number | yes |  |
| `corrections[]` | array<object> | yes |  |
| `corrections[].quantity` | number | yes | Positive adds stock; negative removes stock. |
| `corrections[].productId` | number | yes |  |
| `corrections[].reason` | string | yes |  |
| `corrections[].locationId` | number | yes | Use location 2 for standard inventory management. |
| `corrections[].cost` | object | no | Required when adding stock. |
| `corrections[].cost.currency` | string | no | Required when adding stock. |
| `corrections[].cost.value` | number | no | Per-item cost. Required when adding stock. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `corrections[].batchId` | number | no | Only for removing stock. Omit to use FIFO. |
| `corrections[].orderId` | number | no |  |

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

Through the native Brightpearl API, this operation is `POST /warehouse-service/warehouse/:warehouseId/stock-correction` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-stock-corrections.md) for the provider-specific parameters and requirements.

