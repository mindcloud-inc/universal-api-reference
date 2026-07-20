# Das Keyboard 5Q: Get Signal By Zone

Retrieves a signal by zone ID from Das Keyboard 5Q.

```
GET https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/get-signal-by-zone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Das Keyboard 5Q `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/get-signal-by-zone?connectionId=$CONNECTION_ID&pid=DK5QPID&zoneId=KEY_Q" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pid": "DK5QPID",
  "zoneId": "KEY_Q"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/get-signal-by-zone?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pid` | string | yes | PID of the device to inspect. Example: `DK5QPID`. |
| `zoneId` | string | yes | Keyboard zone to inspect, such as KEY_Q, 74, or 2,2. Example: `KEY_Q`. |

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
| `message` | string | Signal message. |
| `name` | string | Signal name. |
| `pid` | string | Device PID. |
| `updatedAt` | number | Update timestamp in milliseconds. |
| `userId` | number | Q Cloud user ID. |
| `zoneId` | string | Keyboard zone ID. |

## Native endpoint

Through the native Das Keyboard 5Q API, this operation is `GET /signals/pid/:pid/zoneId/:zoneId` (base URL `https://q2.daskeyboard.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signal-by-zone.md) for the provider-specific parameters and requirements.

