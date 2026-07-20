# Utilities - Extract Text between Values with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/ExtractTextBetweenValues`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Extract Text between Values](https://support.encodian.com/hc/en-gb/articles/9604938273565)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text from which a value is to be extracted |
| `startValue` | body | `string` | no | The text value to start the extraction from |
| `endValue` | body | `string` | no | The text value to end the extraction from |
| `ignoreCase` | body | `boolean` | no | Set whether the text case should be ignored when executing the extraction |
| `includeValues` | body | `string` | no | Set whether any or both of the 'Start Value' and 'End Value' should be included within the result Accepted values: `0`, `1`, `2`, `3`. |
| `trimResult` | body | `boolean` | no | Set whether white-space should be trimmed from the extracted string |
