# Set Default Value with Formatting

Sets a default value in the Formatting app.

## Endpoint

- **Method:** `POST`
- **Path:** `/post`
- **Base URL:** `https://postman-echo.com`
- **Official documentation:** [Set Default Value](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/default-value/default-value.ts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | no | The optional input value. |
| `defaultValue` | body | `string` | yes | The fallback value to return when input is empty. |
