# Create a Data Source based visualization with GrowthBook

Creates a data source visualization in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/product-analytics/data-source-exploration`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a Data Source based visualization](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cache` | query | `string` | no | Controls cache behavior for this exploration: `preferred` (default) returns a cached result if one exists, otherwise runs a new query; `never` always runs a new query, ignoring any cached results; `required` only returns a cached result, if none exists returns exploration: null with a message |
| `datasource` | body | `string` | yes | ID of the datasource to query |
| `dimensions[]` | body | `array<object>` | yes | — |
| `chartType` | body | `string` | yes | — |
| `dateRange` | body | `object` | yes | — |
| `type` | body | `string` | yes | — |
| `dataset` | body | `object` | yes | — |
