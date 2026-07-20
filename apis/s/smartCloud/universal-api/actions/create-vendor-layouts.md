# 2Smart Cloud: Create layout



```
POST https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-layouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-layouts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "schema": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-layouts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "schema": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Layout title |
| `schema` | string | yes | Schema JSON string |
| `device_id` | string | no | Optional: id of device taken from product |
| `version` | string | no | Optional: Initial version (0.0.1 by default) |

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

Through the native 2Smart Cloud API, this operation is `POST /vendor/layouts` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-layouts.md) for the provider-specific parameters and requirements.

