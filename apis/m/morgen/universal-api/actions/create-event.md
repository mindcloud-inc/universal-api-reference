# Morgen: Create Event

Creates an event in Morgen.

```
POST https://connect.mindcloud.co/v1/universal/morgen/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morgen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/morgen/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "start": "2026-03-21T14:00:00",
  "duration": "PT30M",
  "timeZone": "America/Argentina/Buenos_Aires",
  "showWithoutTime": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morgen/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "start": "2026-03-21T14:00:00",
    "duration": "PT30M",
    "timeZone": "America/Argentina/Buenos_Aires",
    "showWithoutTime": "false"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | no | Calendar account ID. Defaults to the connection accountId. Default: `{{credentials.accountId}}`. |
| `calendarId` | string | no | Calendar ID. Defaults to the connection calendarId. Default: `{{credentials.calendarId}}`. |
| `title` | string | yes | Event title. |
| `start` | string | yes | LocalDateTime start without timezone offset. Example: `2026-03-21T14:00:00`. |
| `duration` | string | yes | ISO 8601 duration. Example: `PT30M`. |
| `timeZone` | string | yes | IANA timezone, or null for floating events. Example: `America/Argentina/Buenos_Aires`. |
| `showWithoutTime` | boolean | yes | Set true for all-day events. Default: `false`. |
| `description` | string | no | Optional event description. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Morgen API returns.

## Native endpoint

Through the native Morgen API, this operation is `POST /v3/events/create` (base URL `https://api.morgen.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

