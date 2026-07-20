# Count Words with Power Assist

Counts words in a string with Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/string/wordCount`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Count Words](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `string` | body | `string` | yes | The string to count words in. |
| `delimiter` | body | `string` | no | Optional delimiter or regex pattern. Leave blank to split on whitespace. |
