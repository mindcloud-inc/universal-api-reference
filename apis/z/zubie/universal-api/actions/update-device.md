# Zubie: Update Device

Updates an existing device in Zubie.

```
PUT https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string",
  "subscription_status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-device', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string",
    "subscription_status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | yes | Unique device key. |
| `subscription_status` | string | yes | Specify canceled to mark a device as Do Not Renew or active to restore renewal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "serial": "string",
      "status": "string",
      "subscription_status": "string",
      "vehicle_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `serial` | string |  |
| `status` | string |  |
| `subscription_status` | string |  |
| `vehicle_key` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `POST /device/{key}` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-device.md) for the provider-specific parameters and requirements.

