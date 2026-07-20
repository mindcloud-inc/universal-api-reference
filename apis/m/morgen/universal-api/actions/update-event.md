# Morgen: Update Event

Updates an event in Morgen.

```
PUT https://connect.mindcloud.co/v1/universal/morgen/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morgen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/morgen/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morgen/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
| `id` | string | yes | Morgen event ID to update. |
| `title` | string | no | Updated event title. |
| `start` | string | no | LocalDateTime start without timezone offset. Example: `2026-03-21T15:00:00`. |
| `duration` | string | no | ISO 8601 duration. Provide with start/timeZone/showWithoutTime when changing timing. Example: `PT45M`. |
| `timeZone` | string | no | IANA timezone. Provide with start/duration/showWithoutTime when changing timing. Example: `America/Argentina/Buenos_Aires`. |
| `showWithoutTime` | boolean | no | Provide with start/duration/timeZone when changing timing. |
| `description` | string | no | Updated description. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Morgen API returns.

## Native endpoint

Through the native Morgen API, this operation is `POST /v3/events/update` (base URL `https://api.morgen.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

