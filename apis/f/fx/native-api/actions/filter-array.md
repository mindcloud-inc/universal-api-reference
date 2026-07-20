# Filter Array with 1001fx

Filters an array by a comparison operator.

## Endpoint

- **Method:** `POST`
- **Path:** `/array/filterarray`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Filter Array](https://1001fx.com/functions/filterarray)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `criteria` | body | `string` | yes | Value to compare against when filtering. |
| `data[]` | body | `array` | yes | Array of objects to filter. |
| `ignoreCase` | body | `boolean` | no | Whether string filtering should ignore case. |
| `operator` | body | `string` | no | Operator used for the filter comparison. |
| `queryField` | body | `string` | yes | Field name to evaluate in each array item. |
