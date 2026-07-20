# Das Keyboard 5Q: Get Signal Color By Zone

Retrieves a signal color by zone ID from Das Keyboard 5Q.

```
GET https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/get-signal-color-by-zone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Das Keyboard 5Q `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/get-signal-color-by-zone?connectionId=$CONNECTION_ID&pid=DK5QPID&zoneId=KEY_Q" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pid": "DK5QPID",
  "zoneId": "KEY_Q"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/get-signal-color-by-zone?${params}`, {
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
| `zoneId` | string | yes | Keyboard zone whose current color should be fetched. Example: `KEY_Q`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Hex color returned for the device zone, or #000000 when there is no signal. |

## Native endpoint

Through the native Das Keyboard 5Q API, this operation is `GET /signals/pid/:pid/zoneId/:zoneId/color` (base URL `https://q2.daskeyboard.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signal-color-by-zone.md) for the provider-specific parameters and requirements.

