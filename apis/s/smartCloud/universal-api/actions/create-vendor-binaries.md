# 2Smart Cloud: Binary upload



```
POST https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-binaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-binaries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product_version_id": 1,
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-binaries', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "product_version_id": 1,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product_version_id` | number | yes | Id of a product version for which build is uploading |
| `file` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archive_url": "https://example.com",
      "binary_url": "https://example.com",
      "created": "string",
      "firmware_id": 1,
      "id": 1,
      "logs": "string",
      "params": "string",
      "parts": [
        {}
      ],
      "product_id": 1,
      "progress": 1,
      "status": "string",
      "type": "string",
      "updated": "string",
      "vendor_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archive_url` | string |  |
| `binary_url` | string |  |
| `created` | string |  |
| `firmware_id` | number |  |
| `id` | number |  |
| `logs` | string |  |
| `params` | string |  |
| `parts` | array<object> |  |
| `product_id` | number |  |
| `progress` | number |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | string |  |
| `vendor_id` | number |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/binaries` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-binaries.md) for the provider-specific parameters and requirements.

