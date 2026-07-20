# Update Event with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [Update Event](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Events#Goto-EditEvent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EventId` | body | `string` | yes | The event Id to update. |
| `Name` | body | `string` | no | Updated event name. |
| `StartDate` | body | `date` | no | Updated start date and time. |
| `EndDate` | body | `date` | no | Updated end date and time. |
| `IsAllDay` | body | `boolean` | no | Whether this is an all-day event. |
| `Location` | body | `string` | no | Updated event location. |
| `Description` | body | `string` | no | Updated event description. |
| `CalendarId` | body | `string` | no | Updated calendar Id. |
| `RecurrenceRule` | body | `string` | no | Updated RFC5545 recurrence rule. |
| `EndRecurrenceRule` | body | `date` | no | Updated recurrence end date. |
