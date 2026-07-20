# PingBell: Send Notification

Creates a notification for a specific PingBell.

```
POST https://connect.mindcloud.co/v1/universal/pingBell/latest/actions/send-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PingBell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pingBell/latest/actions/send-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pingbellId": "FyUlzEhej6gW0XAUmgL6"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pingBell/latest/actions/send-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pingbellId": "FyUlzEhej6gW0XAUmgL6"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pingbellId` | string | yes | The PingBell ID from the PingBell log URL. Example: `FyUlzEhej6gW0XAUmgL6`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | The PingBell API status response. |

## Native endpoint

Through the native PingBell API, this operation is `POST /log` (base URL `https://app.pingbell.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-notification.md) for the provider-specific parameters and requirements.

