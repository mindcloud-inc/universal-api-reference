# Calculate Average with Power Assist

Calculates an average with Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/math/average`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Calculate Average](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numbers[]` | body | `array<number>` | yes | Array of numbers to average. Numeric strings are allowed when they do not contain formatting such as commas. |
