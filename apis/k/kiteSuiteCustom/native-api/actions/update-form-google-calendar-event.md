# Update Form Google Calendar Event with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/form/integration/google-calendar/events/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Form Google Calendar Event](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | ID of the Google Calendar event to update. |
| `title` | body | `string` | yes | Updated title of the Google Calendar event. |
| `startTime` | body | `string` | yes | Updated ID of the form element representing the start time. |
| `endTime` | body | `string` | yes | Updated ID of the form element representing the end time. |
| `location` | body | `string` | yes | Updated location of the Google Calendar event. |
| `description` | body | `string` | yes | Updated description of the Google Calendar event. |
| `createEventOnEdit` | body | `boolean` | yes | Updated flag to create event on form edit. |
