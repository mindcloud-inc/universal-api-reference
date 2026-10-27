# Update Event with Microsoft 365 Calendar

Updates an existing event in Microsoft 365 Calendar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1.0/me/events/:eventId`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Update Event](https://learn.microsoft.com/en-us/graph/api/event-update?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attendees[].emailAddress` | body | `object` | no | Includes the name and SMTP address of the attendee. |
| `attendees[].emailAddress.address` | body | `string` | no | The email address of the person or entity. |
| `body.content` | body | `string` | no | The content of the item. |
| `end.dateTime` | body | `string` | no | i.e. "2017-04-15T12:00:00" |
| `eventId` | path | `string` | yes | The ID of the Outlook event to update. |
| `location.address` | body | `object` | no | The street address of the location. |
| `location.address.street` | body | `string` | no | — |
| `locations[].address.street` | body | `string` | no | — |
| `locations[].displayName` | body | `string` | no | The name associated with the location. |
| `recurrence.pattern` | body | `object` | no | The frequency of an event.  For access reviews: Do not specify this property for a one-time access review. Only interval, dayOfMonth, and type (weekly, absoluteMonthly) properties of recurrencePattern are supported. |
| `recurrence.pattern.type` | body | `string` | no | — |
| `recurrence.range.type` | body | `string` | no | — |
| `start.dateTime` | body | `string` | no | i.e. "2017-04-15T12:00:00" |
| `subject` | body | `string` | no | The text of the event's subject line. |
| `attendees[].emailAddress.name` | body | `string` | no | The display name of the person or entity. |
| `attendees[].type` | body | `string` | no | The attendee type: required, optional, resource. |
| `body.contentType` | body | `string` | no | The type of the content. Possible values are text and html. |
| `end.timeZone` | body | `string` | no | i.e. "Pacific Standard Time" |
| `importance` | body | `string` | no | The importance of the event. The possible values are: low, normal, high. |
| `location.address.city` | body | `string` | no | — |
| `location.displayName` | body | `string` | no | The name associated with the location. |
| `locations[].address` | body | `object` | no | The street address of the location. |
| `locations[].address.city` | body | `string` | no | — |
| `recurrence.pattern.startDate` | body | `string` | no | — |
| `recurrence.range` | body | `object` | no | The duration of an event. |
| `recurrence.range.startDate` | body | `string` | no | — |
| `start.timeZone` | body | `string` | no | i.e. "Pacific Standard Time" |
| `categories` | body | `string` | no | The categories associated with the event. Send multiple values as a array. |
| `location.address.state` | body | `string` | no | — |
| `location.locationEmailAddress` | body | `string` | no | Optional email address of the location. |
| `locations[].address.state` | body | `string` | no | — |
| `locations[].locationEmailAddress` | body | `string` | no | Optional email address of the location. |
| `recurrence.pattern.endDate` | body | `string` | no | — |
| `recurrence.range.endDate` | body | `string` | no | — |
| `location.address.countryOrRegion` | body | `string` | no | — |
| `location.locationUri` | body | `string` | no | Optional URI representing the location. |
| `locations[].address.countryOrRegion` | body | `string` | no | — |
| `locations[].locationUri` | body | `string` | no | Optional URI representing the location. |
| `sensitivity` | body | `string` | no | The possible values are: normal, personal, private, confidential. |
| `location.address.postalCode` | body | `string` | no | — |
| `locations[].address.postalCode` | body | `string` | no | — |
| `start` | body | `object` | no | The start date, time, and time zone of the event. DateTimeTimeZone |
| `end` | body | `object` | no | The end datetime, and time zone of the event. DateTimeTimeZone |
| `showAs` | body | `string` | no | The status to show. The possible values are: free, tentative, busy, oof, workingElsewhere, unknown. |
| `isOnlineMeeting` | body | `boolean` | no | True if this event has online meeting information, false otherwise. Default is false. Optional. |
| `onlineMeetingProvider` | body | `string` | no | Represents the online meeting service provider. The possible values are teamsForBusiness, skypeForBusiness, and skypeForConsumer. Optional. |
| `isReminderOn` | body | `boolean` | no | Set to true if an alert is set to remind the user of the event. |
| `reminderMinutesBeforeStart` | body | `number` | no | The number of minutes before the event start time that the reminder alert occurs. |
| `isAllDay` | body | `boolean` | no | Set to true if the event lasts all day. |
| `hideAttendees` | body | `boolean` | no | When set to true, each attendee only sees themselves in the meeting request and meeting Tracking list. Default is false. |
| `responseRequested` | body | `boolean` | no | Set to true if the sender would like a response when the event is accepted or declined. |
| `attendees[]` | body | `array` | no | The collection of attendees for the event. |
| `body` | body | `object` | no | The body of the message associated with the event. |
| `location` | body | `object` | no | The location of the event. |
| `locations[]` | body | `array` | no | — |
| `recurrence` | body | `object` | no | The recurrence pattern for the event. |
