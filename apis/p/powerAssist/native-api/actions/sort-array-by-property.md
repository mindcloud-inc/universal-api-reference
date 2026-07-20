# Sort Array By Property with Power Assist

Sorts an array by property with Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/array/sortByProperty`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Sort Array By Property](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `array[]` | body | `array<object>` | yes | Array of objects to sort. |
| `propertyName` | body | `string` | yes | Object property to sort by. |
| `descending` | body | `boolean` | no | Whether to sort in descending order. |
