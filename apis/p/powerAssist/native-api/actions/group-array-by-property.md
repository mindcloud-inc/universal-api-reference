# Group Array By Property with Power Assist

Groups an array by property with Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/array/groupBy`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Group Array By Property](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `array[]` | body | `array<object>` | yes | Array of items to group. |
| `propertyName` | body | `string` | no | Object property to group by. Leave blank for simple values. |
