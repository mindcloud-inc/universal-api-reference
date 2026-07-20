# Hiboutik: List Stock Orders

Retrieves stock orders from Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stock-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stock-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-stock-orders?${params}`, {
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
      "inventoryInputId": 1,
      "storeId": 1,
      "updatedAt": "string",
      "vendorId": 1,
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventoryInputId` | number |  |
| `storeId` | number |  |
| `updatedAt` | string |  |
| `vendorId` | number |  |
| `warehouseId` | number |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /inventory_inputs/` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stock-orders.md) for the provider-specific parameters and requirements.

