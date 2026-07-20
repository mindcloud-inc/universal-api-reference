# Find First Array Item with Power Assist

Finds the first matching array item with Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/array/findFirst`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Find First Array Item](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `array[]` | body | `array<object>` | yes | Array of items to search. |
| `propertyName` | body | `string` | yes | Use this for simple values, or the object property to compare. |
| `comparison` | body | `string` | yes | Comparison operation to apply. |
| `value` | body | `string` | no | Value to compare against. |
| `valueType` | body | `string` | no | Optional type of the comparison value. If blank, the value is treated as a string. |
