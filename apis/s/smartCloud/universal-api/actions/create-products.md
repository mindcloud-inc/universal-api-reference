# 2Smart Cloud: Create Product



```
POST https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "layout_schema": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-products', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "layout_schema": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Product title |
| `layout_schema` | string | yes | JSON schema of layout |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "firmware_id": 1,
      "id": 1,
      "layout_id": 1,
      "mcu": "string",
      "status": "string",
      "title": "string",
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
| `description` | string | Product description |
| `firmware_id` | number | Firmware identifier |
| `id` | number | Product identifier |
| `layout_id` | number | Layout identifier |
| `mcu` | string | Product microcontroller type |
| `status` | string | Product status |
| `title` | string | Product title |
| `vendor_id` | number | Vendor identifier |
| `version` | string | Product version |
| `version_id` | number | Product version identifier |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /products` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-products.md) for the provider-specific parameters and requirements.

