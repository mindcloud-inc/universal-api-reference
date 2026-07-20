# List Events with Zoho Calendar

Retrieves events from a Zoho Calendar calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendars/:calendaruid/events`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [List Events](https://www.zoho.com/calendar/help/api/get-events-list.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Calendar unique identifier. |
| `range` | query | `object` | yes | Date range object for the events query. |
| `byinstance` | query | `boolean` | no | Return recurrence instances individually. |
| `timezone` | query | `string` | no | Timezone for interpreting the response. |
| `crm_event_type` | query | `string` | no | CRM event type filter when applicable. |
