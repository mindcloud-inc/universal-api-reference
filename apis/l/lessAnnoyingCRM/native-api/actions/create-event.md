# Create Event with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [Create Event](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Events#Goto-CreateEvent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Event name. |
| `StartDate` | body | `date` | yes | Start date and time of the event. |
| `EndDate` | body | `date` | yes | End date and time of the event. |
| `IsAllDay` | body | `boolean` | no | Whether this is an all-day event. |
| `Location` | body | `string` | no | Event location. |
| `Description` | body | `string` | no | Event description. |
| `CalendarId` | body | `string` | no | Calendar Id the event belongs to. |
| `IsRecurring` | body | `boolean` | no | Whether the event recurs. |
| `RecurrenceRule` | body | `string` | no | RFC5545 recurrence rule for recurring events. |
| `EndRecurrenceRule` | body | `date` | no | Date the recurrence series should stop. |
