# Browser Use: Create Browser Session

Creates a browser session in Browser Use.

```
POST https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-browser-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-browser-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-browser-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileId` | string | no | Profile ID to use for the browser session. |
| `proxyCountryCode` | string | no | Proxy country code. Defaults to us; null disables proxy. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowResizing` | boolean | no | Whether to allow browser resizing during the session. Default: `false`. |
| `browserScreenHeight` | number | no | Custom browser screen height in pixels. |
| `browserScreenWidth` | number | no | Custom browser screen width in pixels. |
| `enableRecording` | boolean | no | Whether to enable session recording. Default: `false`. |
| `timeout` | number | no | Session timeout in minutes, 1 to 240. Default: `60`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cdpUrl": "https://example.com",
      "id": "string",
      "liveUrl": "https://example.com",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timeoutAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cdpUrl` | string |  |
| `id` | string |  |
| `liveUrl` | string |  |
| `startedAt` | date |  |
| `status` | string |  |
| `timeoutAt` | date |  |

## Native endpoint

Through the native Browser Use API, this operation is `POST /browsers` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-browser-session.md) for the provider-specific parameters and requirements.

