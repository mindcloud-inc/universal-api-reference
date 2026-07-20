# Create Planning Booking with Timewax

Creates a new planning booking in Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `calendar/entries/add/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Create Planning Booking](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231632128)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Required. Booking type: entry for bookings with resources, request for bookings without resources. |
| `resource` | body | `string` | no | Resource code or name for entry bookings. |
| `project` | body | `string` | yes | Required. Code or name of the project. |
| `breakdown` | body | `string` | yes | Required. Code or name of the activity. |
| `date` | body | `date` | yes | Required. Date of the booking, format yyyymmdd or yyyy-mm-dd. |
| `timeFrom` | body | `string` | yes | Required. Start time for the booking, format hh:mm. |
| `hours` | body | `number` | yes | Required. Number of hours. |
