# Put Dataset User with Microsoft Power BI

## Endpoint

- **Method:** `PUT`
- **Path:** `datasets/[:datasetId]/users`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Put Dataset User](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/put-dataset-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `datasetUserAccessRight` | body | `list` | yes | The access rights to assign to the user for the dataset (permission level) |
| `identifier` | body | `string` | yes | For principal type User, provide the *UPN*. Otherwise provide the object ID of the principal. |
| `principalType` | body | `list` | yes | The principal type |
