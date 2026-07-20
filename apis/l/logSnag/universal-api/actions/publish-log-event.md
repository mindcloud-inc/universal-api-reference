# LogSnag: Publish Log Event



```
POST https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/publish-log-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogSnag `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/publish-log-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "channel": "string",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/publish-log-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "channel": "string",
    "event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Project name in LogSnag. |
| `channel` | string | yes | Channel name in LogSnag. |
| `event` | string | yes | Event title to publish. |
| `description` | string | no | Optional event description. |
| `icon` | string | no | Single emoji or emoji shortcode. |
| `notify` | boolean | no | Send a push notification for the event. |
| `parser` | string | no | Parse the description as markdown or plain text. |
| `tags` | object | no | Event tags as key/value pairs. |
| `timestamp` | number | no | Unix timestamp in seconds for historical data. |
| `userId` | string | no | Associate the event with a user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "description": "string",
      "event": "string",
      "icon": "string",
      "notify": true,
      "parser": "string",
      "project": "string",
      "tags": {},
      "timestamp": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string | LogSnag channel name. |
| `description` | string | Event description. |
| `event` | string | Published event title. |
| `icon` | string | Rendered icon or emoji shortcode. |
| `notify` | boolean | Whether LogSnag should notify. |
| `parser` | string | Description parser mode. |
| `project` | string | LogSnag project name. |
| `tags` | object | Event tags. |
| `timestamp` | number | Historical timestamp. |
| `userId` | string | Associated user ID. |

## Native endpoint

Through the native LogSnag API, this operation is `POST /log` (base URL `https://api.logsnag.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-log-event.md) for the provider-specific parameters and requirements.

