# Add Event Reminder with Zoho Connect

Adds a reminder to an event in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/addEventReminder`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Add Event Reminder](https://www.zoho.com/connect/api/add-event-reminder.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `scopeID` | query | `string` | yes |
| `streamId` | query | `string` | yes |
| `intervalDay` | query | `number` | no |
| `intervalMinute` | query | `number` | no |
| `intervalHour` | query | `number` | no |
