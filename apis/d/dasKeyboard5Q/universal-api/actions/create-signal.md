# Das Keyboard 5Q: Create Signal

Creates a signal in Das Keyboard 5Q.

```
POST https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/create-signal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Das Keyboard 5Q `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/create-signal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Apple Stock Increase",
  "zoneId": "KEY_Q",
  "color": "#FF0000",
  "pid": "DK5QPID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/create-signal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Apple Stock Increase",
    "zoneId": "KEY_Q",
    "color": "#FF0000",
    "pid": "DK5QPID"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the signal. Example: `Apple Stock Increase`. |
| `message` | string | no | Message displayed by the signal. Example: `Lucky you! Apple stock is greater than $500`. |
| `zoneId` | string | yes | Keyboard zone targeted by the signal, such as KEY_Q, 74, or 2,2. Example: `KEY_Q`. |
| `color` | string | yes | Signal color as a hex value beginning with # and followed by 3 or 6 hexadecimal digits. Example: `#FF0000`. |
| `effect` | string | no | Visual effect for the signal. Default: `SET_COLOR`. Example: `SET_COLOR`. |
| `pid` | string | yes | PID of the target Das Keyboard device, such as DK5QPID. Example: `DK5QPID`. |
| `clientName` | string | no | Name of the client creating the signal, such as Zapier or Local Node Script. Default: `MindCloud`. Example: `MindCloud`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isArchived` | boolean | no | Whether the signal is archived. Das Keyboard notes this is ignored on localhost. Default: `false`. |
| `isRead` | boolean | no | Whether the signal is marked as read. Das Keyboard notes this is ignored on localhost. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientName": "Ava Chen",
      "color": "string",
      "createdAt": 1,
      "effect": "string",
      "id": 1,
      "isArchived": true,
      "isMuted": true,
      "isRead": true,
      "message": "string",
      "name": "Ava Chen",
      "pid": "string",
      "updatedAt": 1,
      "userId": 1,
      "zoneId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientName` | string | Client that created the signal. |
| `color` | string | Signal color. |
| `createdAt` | number | Creation timestamp in milliseconds. |
| `effect` | string | Signal visual effect. |
| `id` | number | Signal ID. |
| `isArchived` | boolean | Whether the signal is archived. |
| `isMuted` | boolean | Whether the signal is muted in the API response. |
| `isRead` | boolean | Whether the signal is read. |
| `message` | string | Signal message. |
| `name` | string | Signal name. |
| `pid` | string | Device PID. |
| `updatedAt` | number | Update timestamp in milliseconds. |
| `userId` | number | Q Cloud user ID. |
| `zoneId` | string | Keyboard zone ID. |

## Native endpoint

Through the native Das Keyboard 5Q API, this operation is `POST /signals` (base URL `https://q2.daskeyboard.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signal.md) for the provider-specific parameters and requirements.

