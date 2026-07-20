# 2Smart Cloud: Delete product



```
DELETE https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/delete-vendor-products-by-id-delete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/delete-vendor-products-by-id-delete?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/delete-vendor-products-by-id-delete?${params}`, {
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
      "actual_build_id": 1,
      "changelog": "string",
      "created": "string",
      "description": "string",
      "device_id": 1,
      "firmawre": {},
      "firmware_id": 1,
      "firmware_title": "string",
      "icon": "string",
      "id": 1,
      "instruction": "string",
      "is_archived": true,
      "is_custom_frmware": true,
      "is_staging": true,
      "layout": {},
      "layout_id": 1,
      "layout_title": "string",
      "mcu": "string",
      "picture": "string",
      "production_binary_url": "https://example.com",
      "production_build_id": 1,
      "production_version": {},
      "sandbox_build_id": 1,
      "status": "string",
      "title": "string",
      "updated": "string",
      "vendor_id": 1,
      "version": "string",
      "version_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual_build_id` | number |  |
| `changelog` | string |  |
| `created` | string |  |
| `description` | string |  |
| `device_id` | number |  |
| `firmawre` | object |  |
| `firmware_id` | number |  |
| `firmware_title` | string |  |
| `icon` | string |  |
| `id` | number |  |
| `instruction` | string |  |
| `is_archived` | boolean |  |
| `is_custom_frmware` | boolean |  |
| `is_staging` | boolean |  |
| `layout` | object |  |
| `layout_id` | number |  |
| `layout_title` | string |  |
| `mcu` | string |  |
| `picture` | string |  |
| `production_binary_url` | string |  |
| `production_build_id` | number |  |
| `production_version` | object |  |
| `sandbox_build_id` | number |  |
| `status` | string |  |
| `title` | string |  |
| `updated` | string |  |
| `vendor_id` | number |  |
| `version` | string |  |
| `version_id` | number |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/products/{id}/delete` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-vendor-products-by-id-delete.md) for the provider-specific parameters and requirements.

