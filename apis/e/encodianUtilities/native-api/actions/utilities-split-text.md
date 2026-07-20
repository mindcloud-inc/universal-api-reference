# Utilities - Split Text with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/SplitText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Split Text](https://support.encodian.com/hc/en-gb/articles/11846521179805)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text value to process |
| `splitValue` | body | `string` | no | Set the value to split the text provided on |
| `splitOn` | body | `string` | no | Set whether the text should be split on all instances, the first instance or the last instance of the 'Split Value' Accepted values: `0`, `1`, `2`. |
| `trimResult` | body | `boolean` | no | Set whether white-space should be trimmed from the values split from the text provided |
| `removeEmptyValues` | body | `boolean` | no | Set whether empty or null values should be removed from the array of values returned |
| `preserveSplitValue` | body | `boolean` | no | Set whether to preserve the 'Split Value' in each split item returned |
