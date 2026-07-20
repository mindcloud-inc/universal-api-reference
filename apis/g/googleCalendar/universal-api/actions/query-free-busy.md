# Google Calendar: Query Free/Busy

Retrieves free/busy information from Google Calendar.

```
GET https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/query-free-busy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/query-free-busy?connectionId=$CONNECTION_ID&timeMin=2026-05-07T12%3A00%3A00.000Z&timeMax=2026-05-07T12%3A00%3A00.000Z&items%5B0%5D.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timeMin": "2026-05-07T12:00:00.000Z",
  "timeMax": "2026-05-07T12:00:00.000Z",
  "items[0].id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/query-free-busy?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeMin` | date | yes |  |
| `timeMax` | date | yes |  |
| `items[0].id` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Calendar API returns.

## Native endpoint

Through the native Google Calendar API, this operation is `POST freeBusy` (base URL `https://www.googleapis.com/calendar/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-free-busy.md) for the provider-specific parameters and requirements.

