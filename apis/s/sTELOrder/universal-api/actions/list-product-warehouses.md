# STEL Order: List Product Warehouses

Retrieves a list of product warehouses from STEL Order.

```
GET https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-product-warehouses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STEL Order `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-product-warehouses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-product-warehouses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "item-id": 1,
      "item-path": "string",
      "minimum-stock": 1,
      "real-stock": 1,
      "virtual-stock": 1,
      "warehouse-id": 1,
      "warehouse-path": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `item-id` | number |  |
| `item-path` | string |  |
| `minimum-stock` | number |  |
| `real-stock` | number |  |
| `virtual-stock` | number |  |
| `warehouse-id` | number |  |
| `warehouse-path` | string |  |

## Native endpoint

Through the native STEL Order API, this operation is `GET /productWarehouses` (base URL `https://app.stelorder.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-product-warehouses.md) for the provider-specific parameters and requirements.

