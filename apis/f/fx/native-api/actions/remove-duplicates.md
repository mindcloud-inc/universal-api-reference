# Remove Duplicates with 1001fx

Removes duplicate items from an array.

## Endpoint

- **Method:** `POST`
- **Path:** `/array/removeduplicates`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Remove Duplicates](https://1001fx.com/functions/removeduplicates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array` | yes | Array of objects to deduplicate. |
| `fields[]` | body | `array` | no | Fields used to determine duplicate rows. |
| `ignoreCase` | body | `boolean` | no | Whether string comparison should ignore case. |
