# Luxafor: Blink Device

Updates a Luxafor device by blinking it.

```
PUT https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/blink-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Luxafor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/blink-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionFields.color": "red"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/blink-device', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionFields.color": "red"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionFields` | object | no |  |
| `actionFields.color` | string | yes | Accepted colors: red, green, yellow, blue, white, cyan, magenta. Example: `red`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Luxafor API returns.

## Native endpoint

Through the native Luxafor API, this operation is `POST /blink` (base URL `https://api.luxafor.com/webhook/v1/actions`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/blink-device.md) for the provider-specific parameters and requirements.

