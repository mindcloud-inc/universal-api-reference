# 2Smart Cloud: Show layout



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-layouts-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-layouts-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-layouts-by-id?${params}`, {
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
| `id` | number | yes | ID of entity |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "device_id": "string",
      "id": 1,
      "is_archived": true,
      "is_enabled": true,
      "product_status": "string",
      "product_title": "string",
      "product_version": "string",
      "store_id": "string",
      "title": "string",
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
| `created` | string |  |
| `device_id` | string |  |
| `id` | number |  |
| `is_archived` | boolean |  |
| `is_enabled` | boolean |  |
| `product_status` | string |  |
| `product_title` | string |  |
| `product_version` | string |  |
| `store_id` | string |  |
| `title` | string |  |
| `updated` | string |  |
| `vendor_id` | number |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /vendor/layouts/{id}` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vendor-layouts-by-id.md) for the provider-specific parameters and requirements.

