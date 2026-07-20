# Post Dataset User with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `datasets/[:datasetId]/users`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Post Dataset User](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/post-dataset-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `datasetUserAccessRight` | body | `list` | yes | Required. The access right to grant to the user for the dataset. |
| `identifier` | body | `string` | yes | For principal type User, provide the *UPN*. Otherwise provide the object ID of the principal. |
| `principalType` | body | `list` | yes | The principal type |
