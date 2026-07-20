# Prepend To Array with Power Assist

Prepends a value to an array with Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/array/prepend`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Prepend To Array](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `array[]` | body | `array<object>` | yes | Array to prepend to. |
| `value` | body | `string` | yes | Value or array to prepend. |
| `valueType` | body | `string` | no | Optional type of the value. If blank, the value is treated as a string. |
