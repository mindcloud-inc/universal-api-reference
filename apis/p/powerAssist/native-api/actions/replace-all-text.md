# Replace All Text with Power Assist

Replaces all matching text with Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/string/replaceAll`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Replace All Text](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceString` | body | `string` | yes | The string to search within. |
| `searchValue` | body | `string` | yes | Case-sensitive substring to replace. |
| `replaceValue` | body | `string` | yes | Replacement value. |
