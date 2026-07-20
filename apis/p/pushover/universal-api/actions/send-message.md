# Pushover: Send Message



```
POST https://connect.mindcloud.co/v1/universal/pushover/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user": "uQiRzpo4DXghDmr9QzzfQu27cmVRsG",
  "message": "Backup of database \\\"example\\\" finished in 16 minutes."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushover/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user": "uQiRzpo4DXghDmr9QzzfQu27cmVRsG",
    "message": "Backup of database \\\"example\\\" finished in 16 minutes."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user` | string | yes | User key or group key to send the message to. Example: `uQiRzpo4DXghDmr9QzzfQu27cmVRsG`. |
| `message` | string | yes | Message body to push through Pushover. Example: `Backup of database \"example\" finished in 16 minutes.`. |
| `device` | string | no | Optional device name to target instead of all active devices. Example: `droid4`. |
| `title` | string | no | Optional message title. Example: `Backup finished - SQL1`. |
| `priority` | number | no | Message priority from -2 to 2. Example: `0`. |
| `sound` | string | no | Sound name to override the recipient's default tone. Example: `pushover`. |
| `url` | string | no | Supplementary URL to show with the message. Example: `https://example.com/incidents/123`. |
| `urlTitle` | string | no | Optional label shown for the supplementary URL. Example: `Open incident`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timestamp` | number | no | Unix timestamp to display instead of the receipt time. Example: `1331249662`. |
| `ttl` | number | no | Seconds before the message expires and is deleted automatically. Example: `3600`. |
| `html` | number | no | Set to 1 to enable HTML formatting. Example: `1`. |
| `monospace` | number | no | Set to 1 to enable monospace formatting. Example: `1`. |
| `retry` | number | no | Seconds between retries for emergency-priority messages. Example: `60`. |
| `expire` | number | no | Maximum retry window in seconds for emergency-priority messages. Example: `1800`. |
| `callback` | string | no | Public callback URL that Pushover calls when an emergency message is acknowledged. Example: `https://example.com/pushover/callback`. |
| `tags` | string | no | Comma-separated tags stored with an emergency receipt for later cancellation. Example: `s=mail01,r=23,l=chicago`. |
| `attachmentBase64` | string | no | Base64-encoded image attachment. Example: `BASE64_IMAGE_DATA`. |
| `attachmentType` | string | no | MIME type for the Base64 attachment. Example: `image/png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "receipt": "string",
      "request": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `receipt` | string | Emergency receipt identifier returned for priority-2 messages. |
| `request` | string | Pushover request identifier. |
| `status` | number | API status. Returns 1 when the message request succeeds. |

## Native endpoint

Through the native Pushover API, this operation is `POST /messages.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

