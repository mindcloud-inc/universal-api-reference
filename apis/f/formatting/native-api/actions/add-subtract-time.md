# Add/Subtract Time with Formatting

Adds or subtracts time in the Formatting app.

## Endpoint

- **Method:** `POST`
- **Path:** `/post`
- **Base URL:** `https://postman-echo.com`
- **Official documentation:** [Add/Subtract Time](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/add-subtract-time/add-subtract-time.ts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The starting date or time value. |
| `operationMode` | body | `string` | yes | Whether to add or subtract time. |
| `duration` | body | `number` | yes | The amount of time to add or subtract. |
| `unit` | body | `string` | yes | The time unit to apply. |
