# Format Number with Formatting

Formats a number in the Formatting app.

## Endpoint

- **Method:** `POST`
- **Path:** `/post`
- **Base URL:** `https://postman-echo.com`
- **Official documentation:** [Format Number](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/format-number/format-number.ts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `number` | yes | The number to format. |
| `locale` | body | `string` | no | The locale to use for formatting. |
| `maximumFractionDigits` | body | `number` | no | The maximum number of fraction digits. |
