# Execute Queries In Group with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/executeQueries`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Execute Queries In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/execute-queries-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | The dataset ID |
| `queries[]` | body | `array<object>` | yes | The list of dataset queries to execute |
| `impersonatedUserName` | body | `string` | no | The UPN of a user to be impersonated. If the model is not RLS enabled, this will be ignored. |
| `serializerSettings` | body | `object` | no | The serialization settings for the result set |
