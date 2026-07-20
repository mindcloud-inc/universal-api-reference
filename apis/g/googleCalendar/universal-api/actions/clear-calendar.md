# Google Calendar: Clear Calendar

Deletes all events from a primary Google Calendar.

```
DELETE https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/clear-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/clear-calendar?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/clear-calendar?${params}`, {
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
| `calendar` | list | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Calendar API returns.

## Native endpoint

Through the native Google Calendar API, this operation is `POST calendars/:calendar/clear` (base URL `https://www.googleapis.com/calendar/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-calendar.md) for the provider-specific parameters and requirements.

