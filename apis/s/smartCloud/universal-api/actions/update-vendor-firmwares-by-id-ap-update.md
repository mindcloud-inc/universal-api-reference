# 2Smart Cloud: Update firmware



```
PUT https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/update-vendor-firmwares-by-id-ap-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/update-vendor-firmwares-by-id-ap-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/update-vendor-firmwares-by-id-ap-update', {
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
| `ssid` | string | no | Ap ssid |
| `password` | string | no | Ap password |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code_url": "https://example.com",
      "created": "string",
      "id": 1,
      "password": "string",
      "ssid": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code_url` | string |  |
| `created` | string |  |
| `id` | number |  |
| `password` | string |  |
| `ssid` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/firmwares/{id}/ap/update` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vendor-firmwares-by-id-ap-update.md) for the provider-specific parameters and requirements.

