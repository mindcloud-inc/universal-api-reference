# 2Smart Cloud: Update layout



```
PUT https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/update-layouts-by-id-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/update-layouts-by-id-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/update-layouts-by-id-update', {
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
| `title` | string | no | Title for alyout |
| `schema` | string | no | Schema JSON string |

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

Through the native 2Smart Cloud API, this operation is `POST /layouts/{id}/update` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-layouts-by-id-update.md) for the provider-specific parameters and requirements.

