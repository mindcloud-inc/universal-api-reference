# Datadog: Post Event

Creates a new event in Datadog.

```
POST https://connect.mindcloud.co/v1/universal/datadog/latest/actions/post-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/post-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datadog/latest/actions/post-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title of the event. |
| `text` | string | yes | Body text for the event. |
| `aggregationKey` | string | no | Aggregation key for grouping events. |
| `alertType` | string | no | Alert type for the event. |
| `dateHappened` | number | no | POSIX timestamp of the event. |
| `deviceName` | string | no | Device name to associate with the event. |
| `host` | string | no | Host name associated with the event. |
| `priority` | string | no | Priority of the event. |
| `relatedEventId` | number | no | Related event identifier. |
| `sourceTypeName` | string | no | Source type name for the event. |
| `tags[]` | array<string> | no | Tags to attach to the event. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | object | Event returned by Datadog after creation. |
| `status` | string | Status returned by Datadog. |

## Native endpoint

Through the native Datadog API, this operation is `POST /api/v1/events` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-event.md) for the provider-specific parameters and requirements.

