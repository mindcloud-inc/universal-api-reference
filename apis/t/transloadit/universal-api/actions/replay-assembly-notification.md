# Transloadit: Replay Assembly Notification

Replays an assembly notification in Transloadit.

```
POST https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/replay-assembly-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/replay-assembly-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assemblyId": "string",
  "params": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/replay-assembly-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assemblyId": "string",
    "params": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assemblyId` | string | yes | The assembly ID whose notification should be replayed. |
| `params` | string | yes | JSON string required by Transloadit when replaying an assembly notification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "notification_id": "string",
      "ok": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notification_id` | string | Identifier of the replayed notification event. |
| `ok` | string | Status code returned by Transloadit for assembly notification replay. |
| `success` | boolean | Whether the notification replay request succeeded. |

## Native endpoint

Through the native Transloadit API, this operation is `POST /assembly_notifications/:assemblyId/replay` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replay-assembly-notification.md) for the provider-specific parameters and requirements.

