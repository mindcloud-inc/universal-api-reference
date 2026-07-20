# Utilities - Array Contains Value with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/ArrayContainsValue`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Array Contains Value](https://support.encodian.com/hc/en-gb/articles/10242960376476)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | yes | The JSON data to evaluate |
| `value` | body | `string` | yes | The value to check is contained within the array |
| `path` | body | `string` | no | Select a specific node within the 'Data' using a JSONPath expression |
| `ignoreCase` | body | `boolean` | no | Set whether text case should be ignored when searching the array |
