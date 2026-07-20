# Create calendar with AddEvent

## Endpoint

- **Method:** `POST`
- **Path:** `/calendars`
- **Base URL:** `https://api.addevent.com/calevent/v2`
- **Official documentation:** [Create calendar](https://docs.addevent.com/reference/create-calendar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | The calendar title. |
| `timezone` | body | `string` | no | Default timezone for events created on this calendar. |
| `weekday_begin` | body | `string` | no | Day of the week that the calendar starts on. |
| `description` | body | `string` | no | Calendar description shown on the landing page. |
| `internal_name` | body | `string` | no | Internal-only calendar name. |
| `calendar_color` | body | `number` | no | Calendar color value from the account palette. |
| `landing_page_template_id` | body | `string` | no | Custom landing page template ID or default. |
| `embeddable_calendar_template_id` | body | `string` | no | Custom embeddable calendar template ID or default. |
| `custom_data` | body | `object` | no | Structured key-value data attached to the calendar. |
