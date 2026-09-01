# Amark: Get Product Info



```
GET https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-product-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-product-info?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-product-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |

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
        "imageURL": "https://example.com",
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
| `successData.imageURL` | string |  |
| `successData.packageUnits` | number |  |
| `successData.productModifyId` | number |  |
| `successData.sku` | string |  |
| `successData.troyOz` | number |  |
| `successData.type` | string |  |
| `successData.weightOz` | number |  |

## Native endpoint

Through the native Amark API, this operation is `POST /Product/Info` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-info.md) for the provider-specific parameters and requirements.

