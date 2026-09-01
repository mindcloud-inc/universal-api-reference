# Amark: Bulk Update Products



```
PUT https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/bulk-update-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/bulk-update-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/bulk-update-products', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "context": "string",
      "event": "string",
      "status": 1,
      "successData": {
        "description": "string",
        "id": 1,
        "packageUnits": 1,
        "productModifyId": 1,
        "sku": "string",
        "troyOz": 1,
        "type": "string",
        "weightOz": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | string |  |
| `event` | string |  |
| `status` | number |  |
| `successData.description` | string |  |
| `successData.id` | number |  |
| `successData.packageUnits` | number |  |
| `successData.productModifyId` | number |  |
| `successData.sku` | string |  |
| `successData.troyOz` | number |  |
| `successData.type` | string |  |
| `successData.weightOz` | number |  |

## Native endpoint

Through the native Amark API, this operation is `POST /Product/BulkModify` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-products.md) for the provider-specific parameters and requirements.

