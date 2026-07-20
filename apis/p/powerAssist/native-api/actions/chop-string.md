# Chop String with Power Assist

Chops a string into chunks with Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/string/chop`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Chop String](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `string` | body | `string` | yes | The string to break into chunks. |
| `interval` | body | `number` | yes | The size of each chunk. |
