# Create a fact metric analysis with GrowthBook

Creates a fact metric analysis in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/fact-metrics/:id/analysis`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a fact metric analysis](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The fact metric id to analyze |
| `userIdType` | body | `string` | no | The identifier type to use for the analysis. If not provided, defaults to the first available identifier type in the fact table. |
| `lookbackDays` | body | `number` | no | Number of days to look back for the analysis. Defaults to 30. |
| `populationType` | body | `string` | no | The type of population to analyze. Defaults to 'factTable', meaning the analysis will return the metric value for all units found in the fact table. |
| `populationId` | body | `string` | no | — |
| `additionalNumeratorFilters` | body | `list<string>` | no | We support passing in adhoc filters for an analysis that don't live on the metric itself. These are in addition to the metric's filters. To use this, you can pass in an array of Fact Table Filter Ids. |
| `additionalDenominatorFilters` | body | `list<string>` | no | We support passing in adhoc filters for an analysis that don't live on the metric itself. These are in addition to the metric's filters. To use this, you can pass in an array of Fact Table Filter Ids. |
| `useCache` | body | `boolean` | no | Whether to use a cached query if one exists. Defaults to true. |
