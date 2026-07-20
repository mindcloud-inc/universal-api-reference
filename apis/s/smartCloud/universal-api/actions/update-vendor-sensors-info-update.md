# 2Smart Cloud: Sensor info update



```
PUT https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/update-vendor-sensors-info-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/update-vendor-sensors-info-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/update-vendor-sensors-info-update', {
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
| `product_version_id` | number | no | Product version id |
| `sensor` | string | no | Sensor topic |
| `info` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "description": "string",
      "id": 1,
      "language": "string",
      "possible_value": "string",
      "product_id": 1,
      "sensor": "string",
      "title": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `description` | string |  |
| `id` | number |  |
| `language` | string |  |
| `possible_value` | string |  |
| `product_id` | number |  |
| `sensor` | string |  |
| `title` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/sensors-info/update` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vendor-sensors-info-update.md) for the provider-specific parameters and requirements.

