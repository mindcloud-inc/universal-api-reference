# Execute Dax Queries In Group with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/executeDaxQueries`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Execute Dax Queries In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/execute-dax-queries-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | The dataset ID |
| `query` | body | `string` | yes | Query text. |
| `applicationContext` | body | `string` | no | JSON structure containing additional information about an operation. |
| `culture` | body | `string` | no | Culture code that controls locale-specific query formatting, such as en-US. For more information about supported culture codes, see Supported languages and countries/regions for Power BI. |
| `customData` | body | `string` | no | Custom data for use in Dynamic RLS. For example, North America can be referenced by the model's CUSTOMDATA() function. |
| `effectiveUsername` | body | `string` | no | Effective username for the query. |
| `memoryLimit` | body | `number` | no | Memory limit (in KB) for the query. |
| `queryTimeout` | body | `number` | no | Query timeout in seconds. |
| `resultSetRowCountLimit` | body | `number` | no | Maximum number of rows to return. Default is 1,000,000 rows. |
| `roles[]` | body | `array<string>` | no | Roles assigned to the user. |
| `schemaOnly` | body | `boolean` | no | Whether the query must return only the schema. |
