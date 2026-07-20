# RotaCloud: Launch Active Terminal

Launches a terminal in RotaCloud.

```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/launch-active-terminal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/launch-active-terminal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "device": "string",
  "terminal": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/launch-active-terminal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "device": "string",
    "terminal": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `device` | string | yes | Device name or identifier. |
| `terminal` | number | yes | Terminal ID to launch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "debug": true,
      "default_location": {},
      "deleted": true,
      "device": "string",
      "id": 1,
      "ip": "string",
      "location": {},
      "name": "Ava Chen",
      "platform": "string",
      "require_photo": true,
      "require_photo_breaks": true,
      "secret": "string",
      "server_time": 1,
      "timezone": 1,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `debug` | boolean |  |
| `default_location` | object |  |
| `deleted` | boolean |  |
| `device` | string |  |
| `id` | number |  |
| `ip` | string |  |
| `location` | object |  |
| `name` | string |  |
| `platform` | string |  |
| `require_photo` | boolean |  |
| `require_photo_breaks` | boolean |  |
| `secret` | string |  |
| `server_time` | number |  |
| `timezone` | number |  |
| `version` | string |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/terminals_active` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/launch-active-terminal.md) for the provider-specific parameters and requirements.

