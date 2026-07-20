# Utilities - Array Remove Duplicates with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/ArrayRemoveDuplicates`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Array Remove Duplicates](https://support.encodian.com/hc/en-gb/articles/10614334072476)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | yes | The JSON data to modify |
| `ignoreCase` | body | `boolean` | yes | Set whether the text case should be ignored when searching for duplicates |
| `path` | body | `string` | no | Select a specific node within the 'Data' using a JSONPath expression |
