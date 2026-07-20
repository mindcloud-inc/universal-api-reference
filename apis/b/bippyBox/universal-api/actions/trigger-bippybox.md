# BippyBox: Trigger BippyBox

Triggers a BippyBox device with audio and color.

```
POST https://connect.mindcloud.co/v1/universal/bippyBox/latest/actions/trigger-bippybox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BippyBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bippyBox/latest/actions/trigger-bippybox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "string",
  "deviceId": "string",
  "url": "https://example.com",
  "color": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bippyBox/latest/actions/trigger-bippybox', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "string",
    "deviceId": "string",
    "url": "https://example.com",
    "color": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uid` | string | yes | Your BippyBox UID used to authenticate the request. |
| `deviceId` | string | yes | The ID of the synced BippyBox device to trigger. |
| `url` | string | yes | A hosted OGG audio file URL to play on the BippyBox. |
| `color` | string | yes | Hex color for the trigger effect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error message returned when the request fails. |
| `message` | string | Command acknowledgement returned when the box is triggered. |
| `status` | string | Connection status returned by the API. |

## Native endpoint

Through the native BippyBox API, this operation is `POST https://mqtt.bippybox.io/send` (base URL `https://app.bippybox.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-bippybox.md) for the provider-specific parameters and requirements.

