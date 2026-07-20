# Execute Queries with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `datasets/[:datasetId]/executeQueries`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Execute Queries](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/execute-queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `queries[]` | body | `array<object>` | yes | The list of dataset queries to execute |
| `impersonatedUserName` | body | `string` | no | The UPN of a user to be impersonated. If the model is not RLS enabled, this will be ignored. |
| `serializerSettings` | body | `object` | no | The serialization settings for the result set |
