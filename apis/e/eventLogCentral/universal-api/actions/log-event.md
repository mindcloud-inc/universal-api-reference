# EventLogCentral: Log Event

Creates an event in EventLogCentral.

```
POST https://connect.mindcloud.co/v1/universal/eventLogCentral/latest/actions/log-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventLogCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventLogCentral/latest/actions/log-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventLogCentral/latest/actions/log-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes |  |
| `title` | string | no |  |
| `description` | string | no |  |
| `author` | string | no |  |
| `category` | string | no |  |
| `notes` | string | no |  |
| `data` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean | Whether the event log request succeeded. |

## Native endpoint

Through the native EventLogCentral API, this operation is `POST /api/logEvent` (base URL `https://api.eventlogcentral.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/log-event.md) for the provider-specific parameters and requirements.

