# Utilities - Format Text Case with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/FormatTextCase`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Format Text Case](https://support.encodian.com/hc/en-gb/articles/11009856518557)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text value to format |
| `action` | body | `string` | yes | The formatting action to apply to the text value provided Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `cultureName` | body | `string` | no | Change the thread culture used to process the request. |
