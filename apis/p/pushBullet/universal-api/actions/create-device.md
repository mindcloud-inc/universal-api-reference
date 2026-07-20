# Pushbullet: Create Device

Creates a new device in Pushbullet.

```
POST https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nickname": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-device', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nickname": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nickname` | string | yes | Nickname for the device. |
| `type` | string | yes | Device type (for example stream). |

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

Through the native Pushbullet API, this operation is `POST /devices` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-device.md) for the provider-specific parameters and requirements.

