# Zoho Calendar: Delete Event

Deletes an existing event from Zoho Calendar.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/delete-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/delete-event?connectionId=$CONNECTION_ID&calendarUid=string&eventUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarUid": "string",
  "eventUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCalendar/latest/actions/delete-event?${params}`, {
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
| `eventUid` | string | yes | Event unique identifier. |
| `eventData` | object | no | Zoho's live delete endpoint requires `eventData.uid` and `eventData.etag` from a prior event read response, even for standard single-event deletes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {
          "caluid": "string",
          "estatus": "string",
          "uid": "string"
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
| `events[].estatus` | string |  |
| `events[].uid` | string |  |

## Native endpoint

Through the native Zoho Calendar API, this operation is `DELETE /calendars/:calendaruid/events/:eventuid` (base URL `https://calendar.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-event.md) for the provider-specific parameters and requirements.

