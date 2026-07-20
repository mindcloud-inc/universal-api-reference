# AddEvent: Delete calendar



```
DELETE https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/delete-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/delete-calendar?connectionId=$CONNECTION_ID&calendarId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/delete-calendar?${params}`, {
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
| `calendarId` | string | yes | Unique identifier for the calendar. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AddEvent API returns.

## Native endpoint

Through the native AddEvent API, this operation is `DELETE /calendars/:calendar_id` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-calendar.md) for the provider-specific parameters and requirements.

