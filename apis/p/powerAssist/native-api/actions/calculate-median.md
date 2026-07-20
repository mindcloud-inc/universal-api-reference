# Calculate Median with Power Assist

Calculates a median with Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/math/median`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Calculate Median](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numbers[]` | body | `array<number>` | yes | Array of numbers to calculate the median from. Numeric strings are allowed when they do not contain formatting such as commas. |
