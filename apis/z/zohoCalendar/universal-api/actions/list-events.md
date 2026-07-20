# Zoho Calendar: List Events

Retrieves events from a Zoho Calendar calendar.

```
GET https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/list-events?connectionId=$CONNECTION_ID&calendarUid=string&range=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarUid": "string",
  "range": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/list-events?${params}`, {
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
| `calendarUid` | string | yes | Calendar unique identifier. |
| `range` | object | yes | Date range object for the events query. |
| `byInstance` | boolean | no | Return recurrence instances individually. |
| `timezone` | string | no | Timezone for interpreting the response. |
| `crmEventType` | string | no | CRM event type filter when applicable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {
          "caluid": "string",
          "dateandtime": {
            "end": "string",
            "start": "string",
            "timezone": "string"
          },
          "etag": "string",
          "isallday": true,
          "isApproved": true,
          "location": "string",
          "organizer": "string",
          "recurrenceid": "string",
          "title": "string",
          "uid": "string",
          "viewEventURL": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[].caluid` | string |  |
| `events[].dateandtime.end` | string |  |
| `events[].dateandtime.start` | string |  |
| `events[].dateandtime.timezone` | string |  |
| `events[].etag` | string |  |
| `events[].isallday` | boolean |  |
| `events[].isApproved` | boolean |  |
| `events[].location` | string |  |
| `events[].organizer` | string |  |
| `events[].recurrenceid` | string |  |
| `events[].title` | string |  |
| `events[].uid` | string |  |
| `events[].viewEventURL` | string |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `GET /calendars/:calendaruid/events` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

