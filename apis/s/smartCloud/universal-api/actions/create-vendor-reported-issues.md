# 2Smart Cloud: Report vendor issue



```
POST https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-reported-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-reported-issues" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-reported-issues', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Issue type |
| `message` | string | yes | Message describing issue |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "id": 1,
      "message": "string",
      "product_id": 1,
      "status": "string",
      "type": "string",
      "updated": "string",
      "user_id": 1,
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
| `id` | number |  |
| `message` | string |  |
| `product_id` | number |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | string |  |
| `user_id` | number |  |
| `vendor_id` | number |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/reported-issues` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-reported-issues.md) for the provider-specific parameters and requirements.

