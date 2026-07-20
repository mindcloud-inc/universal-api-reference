# Utilities - Compare Text with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/CompareText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Compare Text](https://support.encodian.com/hc/en-gb/articles/11782390540957)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `primaryText` | body | `string` | yes | The first text value to compare |
| `secondaryText` | body | `string` | yes | The second text value to compare |
| `ignoreCase` | body | `boolean` | no | Set whether text case should be ignored when comparing the text values provided |
