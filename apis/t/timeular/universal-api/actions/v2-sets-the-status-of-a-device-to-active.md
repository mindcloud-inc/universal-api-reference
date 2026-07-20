# Timeular: V2 Sets the status of a Device to active

Sets a device as active in the Timeular v2 API.

```
POST https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-sets-the-status-of-a-device-to-active
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-sets-the-status-of-a-device-to-active" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deviceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-sets-the-status-of-a-device-to-active', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deviceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "disabled": true,
      "name": "Ava Chen",
      "serial": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `disabled` | boolean |  |
| `name` | string |  |
| `serial` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `POST /api/v2/devices/:deviceId/active` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-sets-the-status-of-a-device-to-active.md) for the provider-specific parameters and requirements.

