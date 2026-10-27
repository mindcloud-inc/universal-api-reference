# Microsoft 365 Calendar: Create Event

Updates an existing event in Microsoft 365 Calendar.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/create-event2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Calendar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/create-event2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Calendar/latest/actions/create-event2', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attendees[].emailAddress` | object | no | Includes the name and SMTP address of the attendee. |
| `attendees[].emailAddress.address` | string | no | The email address of the person or entity. |
| `body.content` | string | no | The content of the item. |
| `end.dateTime` | string | no | i.e. "2017-04-15T12:00:00" |
| `location.address` | object | no | The street address of the location. |
| `location.address.street` | string | no |  |
| `locations[].address.street` | string | no |  |
| `locations[].displayName` | string | no | The name associated with the location. |
| `recurrence.pattern` | object | no | The frequency of an event. For access reviews: Do not specify this property for a one-time access review. Only interval, dayOfMonth, and type (weekly, absoluteMonthly) properties of recurrencePattern are supported. |
| `recurrence.pattern.type` | string | no |  |
| `recurrence.range.type` | string | no |  |
| `start.dateTime` | string | no | i.e. "2017-04-15T12:00:00" |
| `subject` | string | no | The text of the event's subject line. Example: `Updated MindCloud calendar test event`. |
| `attendees[].emailAddress.name` | string | no | The display name of the person or entity. |
| `attendees[].type` | string | no | The attendee type: required, optional, resource. |
| `body.contentType` | string | no | The type of the content. Possible values are text and html. |
| `end.timeZone` | string | no | i.e. "Pacific Standard Time" |
| `importance` | string | no | The importance of the event. The possible values are: low, normal, high. |
| `location.address.city` | string | no |  |
| `location.displayName` | string | no | The name associated with the location. |
| `locations[].address` | object | no | The street address of the location. |
| `locations[].address.city` | string | no |  |
| `recurrence.pattern.startDate` | string | no |  |
| `recurrence.range` | object | no | The duration of an event. |
| `recurrence.range.startDate` | string | no |  |
| `start.timeZone` | string | no | i.e. "Pacific Standard Time" |
| `categories` | string | no | The categories associated with the event. Accepts multiple values as an array. |
| `location.address.state` | string | no |  |
| `location.locationEmailAddress` | string | no | Optional email address of the location. |
| `locations[].address.state` | string | no |  |
| `locations[].locationEmailAddress` | string | no | Optional email address of the location. |
| `recurrence.pattern.endDate` | string | no |  |
| `recurrence.range.endDate` | string | no |  |
| `location.address.countryOrRegion` | string | no |  |
| `location.locationUri` | string | no | Optional URI representing the location. |
| `locations[].address.countryOrRegion` | string | no |  |
| `locations[].locationUri` | string | no | Optional URI representing the location. |
| `sensitivity` | string | no | The possible values are: normal, personal, private, confidential. |
| `location.address.postalCode` | string | no |  |
| `locations[].address.postalCode` | string | no |  |
| `start` | object | no | The start date, time, and time zone of the event. DateTimeTimeZone |
| `end` | object | no | The end datetime, and time zone of the event. DateTimeTimeZone |
| `showAs` | string | no | The status to show. The possible values are: free, tentative, busy, oof, workingElsewhere, unknown. |
| `isOnlineMeeting` | boolean | no | True if this event has online meeting information, false otherwise. Default is false. Optional. |
| `onlineMeetingProvider` | string | no | Represents the online meeting service provider. The possible values are teamsForBusiness, skypeForBusiness, and skypeForConsumer. Optional. |
| `isReminderOn` | boolean | no | Set to true if an alert is set to remind the user of the event. |
| `reminderMinutesBeforeStart` | number | no | The number of minutes before the event start time that the reminder alert occurs. |
| `isAllDay` | boolean | no | Set to true if the event lasts all day. |
| `hideAttendees` | boolean | no | When set to true, each attendee only sees themselves in the meeting request and meeting Tracking list. Default is false. |
| `responseRequested` | boolean | no | Set to true if the sender would like a response when the event is accepted or declined. |
| `allowNewTimeProposals` | boolean | no | true if attendees can propose new times for this event. |
| `attendees[]` | array | no | The collection of attendees for the event. |
| `body` | object | no | The body of the message associated with the event. |
| `location` | object | no | The location of the event. |
| `locations[]` | array | no |  |
| `recurrence` | object | no | The recurrence pattern for the event. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bodyPreview": "string",
      "end": {
        "dateTime": "string",
        "timeZone": "string"
      },
      "id": "string",
      "isAllDay": true,
      "isCancelled": true,
      "location": {
        "displayName": "Ava Chen"
      },
      "organizer": {
        "emailAddress": {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      },
      "start": {
        "dateTime": "string",
        "timeZone": "string"
      },
      "subject": "string",
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bodyPreview` | string | Plain-text preview of the event body. |
| `end.dateTime` | string | Event end date and time. |
| `end.timeZone` | string | Event end time zone. |
| `id` | string | Event ID. |
| `isAllDay` | boolean | Whether the event lasts all day. |
| `isCancelled` | boolean | Whether the event is cancelled. |
| `location.displayName` | string | Event location display name. |
| `organizer.emailAddress.address` | string | Organizer email address. |
| `organizer.emailAddress.name` | string | Organizer display name. |
| `start.dateTime` | string | Event start date and time. |
| `start.timeZone` | string | Event start time zone. |
| `subject` | string | Event subject. |
| `webLink` | string | Outlook web URL for the event. |

## Native endpoint

Through the native Microsoft 365 Calendar API, this operation is `PATCH /v1.0/me/events` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event2.md) for the provider-specific parameters and requirements.

