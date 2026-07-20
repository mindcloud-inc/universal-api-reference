# Pushbullet: Update Device

Updates an existing device in Pushbullet.

```
PUT https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/update-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/update-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "device_iden": "string",
  "nickname": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/update-device', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "device_iden": "string",
    "nickname": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `device_iden` | string | yes | Device identifier to update. |
| `nickname` | string | yes | Updated nickname for the device. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created": 1,
      "iden": "string",
      "manufacturer": "string",
      "model": "string",
      "modified": 1,
      "nickname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | number |  |
| `iden` | string |  |
| `manufacturer` | string |  |
| `model` | string |  |
| `modified` | number |  |
| `nickname` | string |  |

## Native endpoint

Through the native Pushbullet API, this operation is `POST /devices/:device_iden` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-device.md) for the provider-specific parameters and requirements.

