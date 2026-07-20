# Split String Into Words with Power Assist

Splits a string into words with Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/string/words`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Split String Into Words](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `string` | body | `string` | yes | The string to split. |
| `delimiter` | body | `string` | no | Optional delimiter or regex pattern. Leave blank to split on whitespace. |
