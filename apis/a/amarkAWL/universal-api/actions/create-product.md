# Amark: Create Product



```
POST https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "sku": "string",
  "description": "string",
  "type": "string",
  "troyOz": 1,
  "weightOz": 1,
  "packageUnits": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "sku": "string",
    "description": "string",
    "type": "string",
    "troyOz": 1,
    "weightOz": 1,
    "packageUnits": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `sku` | string | yes |  |
| `description` | string | yes |  |
| `type` | string | yes |  |
| `troyOz` | number | yes |  |
| `weightOz` | number | yes |  |
| `packageUnits` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageURL` | string | no |  |

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

Through the native Amark API, this operation is `POST /Product/Create` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

