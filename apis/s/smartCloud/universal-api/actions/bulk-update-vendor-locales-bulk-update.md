# 2Smart Cloud: Bulk Update locales



```
PUT https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/bulk-update-vendor-locales-bulk-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/bulk-update-vendor-locales-bulk-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/bulk-update-vendor-locales-bulk-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array<object> | no |  |
| `data[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "language": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `language` | string |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/locales/bulk-update` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-vendor-locales-bulk-update.md) for the provider-specific parameters and requirements.

