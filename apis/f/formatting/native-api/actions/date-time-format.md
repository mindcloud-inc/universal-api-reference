# Date/Time Format with Formatting

Formats a date or time in the Formatting app.

## Endpoint

- **Method:** `POST`
- **Path:** `/post`
- **Base URL:** `https://postman-echo.com`
- **Official documentation:** [Date/Time Format](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/date-time-format/date-time-format.ts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The date or time value to format. |
| `outputFormat` | body | `string` | yes | The output date format pattern. |
