# Utilities - Replace Value with Text with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/ReplaceValueWithText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Replace Value with Text](https://support.encodian.com/hc/en-gb/articles/11774858455709)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text value to process |
| `searchText` | body | `string` | no | The text to locate and replace with the 'Replacement Text' value, a blank value is treated as white-space |
| `replacementText` | body | `string` | no | The text to replace the matched values with, a blank value will remove the matched text values |
| `trimResult` | body | `boolean` | no | Set whether white-space should be trimmed from the processed text value |
| `ignoreCase` | body | `boolean` | no | Set whether text case should be ignored when searching the text value |
