# 2Smart Cloud: Unstage product



```
PUT https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/unstage-vendor-products-by-id-unstage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/unstage-vendor-products-by-id-unstage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/unstage-vendor-products-by-id-unstage', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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

Through the native 2Smart Cloud API, this operation is `POST /vendor/products/{id}/unstage` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unstage-vendor-products-by-id-unstage.md) for the provider-specific parameters and requirements.

