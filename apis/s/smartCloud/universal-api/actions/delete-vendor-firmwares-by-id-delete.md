# 2Smart Cloud: Delete firmware



```
DELETE https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/delete-vendor-firmwares-by-id-delete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/delete-vendor-firmwares-by-id-delete?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/delete-vendor-firmwares-by-id-delete?${params}`, {
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
      "config": "string",
      "created": "string",
      "firmware_base": "string",
      "id": 1,
      "is_archived": true,
      "product_status": "string",
      "product_title": "string",
      "product_version": "string",
      "title": "string",
      "updated": "string",
      "vendor_id": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | string |  |
| `created` | string |  |
| `firmware_base` | string |  |
| `id` | number |  |
| `is_archived` | boolean |  |
| `product_status` | string |  |
| `product_title` | string |  |
| `product_version` | string |  |
| `title` | string |  |
| `updated` | string |  |
| `vendor_id` | number |  |
| `version` | number |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/firmwares/{id}/delete` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-vendor-firmwares-by-id-delete.md) for the provider-specific parameters and requirements.

