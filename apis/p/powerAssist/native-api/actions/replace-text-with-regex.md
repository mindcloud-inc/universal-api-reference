# Replace Text With Regex with Power Assist

Replaces text by regex in Power Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/string/regexReplace`
- **Base URL:** `https://power-assist.p.rapidapi.com`
- **Official documentation:** [Replace Text With Regex](https://rapidapi.com/elevate-digital-elevate-digital-default/api/power-assist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceString` | body | `string` | yes | The string to search within. |
| `pattern` | body | `string` | yes | Regex pattern with leading and trailing slash, optionally followed by flags, for example /\\d+/gi. |
| `replaceValue` | body | `string` | yes | Replacement value to insert for each match. |
