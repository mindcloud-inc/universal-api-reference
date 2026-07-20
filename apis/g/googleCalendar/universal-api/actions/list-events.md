# Google Calendar: List Events

Retrieves events from a Google Calendar calendar.

```
GET https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Calendar `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0&calendar=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "calendar": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/list-events?${params}`, {
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
| `calendar` | list | yes |  |
| `timeMin` | date | no | Lower bound (exclusive) for an event's end time to filter by. |
| `timeMax` | date | no | Upper bound (exclusive) for an event's start time to filter by. |
| `q` | string | no |  |
| `updatedMin` | date | no | Lower bound for an event's last modification time to filter by. |
| `showDeleted` | boolean | no | Default: `false`. |
| `showHiddenInvitations` | boolean | no | Default: `false`. |
| `singleEvents` | boolean | no | Whether to expand recurring events into instances and only return single one-off events and instances of recurring events, but not the underlying recurring events themselves. Optional. The default is False. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {
          "email": "ava@example.com",
          "responseStatus": "string",
          "self": true
        }
      ],
      "conferenceData": {
        "conferenceId": "string",
        "conferenceSolution": {
          "iconUri": "string",
          "key": {
            "type": "string"
          },
          "name": "Ava Chen"
        },
        "entryPoints": [
          {
            "entryPointType": "string",
            "label": "string",
            "uri": "string"
          }
        ]
      },
      "created": "string",
      "creator": {
        "email": "ava@example.com"
      },
      "end": {
        "dateTime": "string",
        "timeZone": "string"
      },
      "etag": "string",
      "eventType": "string",
      "hangoutLink": "https://example.com",
      "htmlLink": "https://example.com",
      "iCalUID": "string",
      "id": "string",
      "kind": "string",
      "organizer": {
        "email": "ava@example.com"
      },
      "reminders": {
        "useDefault": true
      },
      "sequence": 1,
      "start": {
        "dateTime": "string",
        "timeZone": "string"
      },
      "status": "string",
      "summary": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees[].email` | string |  |
| `attendees[].responseStatus` | string |  |
| `attendees[].self` | boolean |  |
| `conferenceData.conferenceId` | string |  |
| `conferenceData.conferenceSolution.iconUri` | string |  |
| `conferenceData.conferenceSolution.key.type` | string |  |
| `conferenceData.conferenceSolution.name` | string |  |
| `conferenceData.entryPoints[].entryPointType` | string |  |
| `conferenceData.entryPoints[].label` | string |  |
| `conferenceData.entryPoints[].uri` | string |  |
| `created` | string |  |
| `creator.email` | string |  |
| `end.dateTime` | string |  |
| `end.timeZone` | string |  |
| `etag` | string |  |
| `eventType` | string |  |
| `hangoutLink` | string |  |
| `htmlLink` | string |  |
| `iCalUID` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `organizer.email` | string |  |
| `reminders.useDefault` | boolean |  |
| `sequence` | number |  |
| `start.dateTime` | string |  |
| `start.timeZone` | string |  |
| `status` | string |  |
| `summary` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Google Calendar API, this operation is `GET calendars/:calendar/events` (base URL `https://www.googleapis.com/calendar/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

