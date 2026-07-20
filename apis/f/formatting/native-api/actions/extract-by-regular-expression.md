# Extract by Regular Expression with Formatting

Extracts text by regular expression in the Formatting app.

## Endpoint

- **Method:** `POST`
- **Path:** `/post`
- **Base URL:** `https://postman-echo.com`
- **Official documentation:** [Extract by Regular Expression](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/extract-by-regex/extract-by-regex.ts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The text to search. |
| `regExpString` | body | `string` | yes | The regular expression pattern. |
| `flags` | body | `string` | no | The regex flags to apply. |
