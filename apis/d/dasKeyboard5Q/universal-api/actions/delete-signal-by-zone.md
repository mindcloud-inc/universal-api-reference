# Das Keyboard 5Q: Delete Signal By Zone

Deletes a signal by zone ID from Das Keyboard 5Q.

```
DELETE https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/delete-signal-by-zone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Das Keyboard 5Q `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/delete-signal-by-zone?connectionId=$CONNECTION_ID&pid=DK5QPID&zoneId=KEY_Q" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pid": "DK5QPID",
  "zoneId": "KEY_Q"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/delete-signal-by-zone?${params}`, {
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
| `pid` | string | yes | PID of the device whose zone signal should be deleted. Example: `DK5QPID`. |
| `zoneId` | string | yes | Keyboard zone whose signal should be deleted. Example: `KEY_Q`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Das Keyboard 5Q API returns.

## Native endpoint

Through the native Das Keyboard 5Q API, this operation is `DELETE /signals/pid/:pid/zoneId/:zoneId` (base URL `https://q2.daskeyboard.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-signal-by-zone.md) for the provider-specific parameters and requirements.

