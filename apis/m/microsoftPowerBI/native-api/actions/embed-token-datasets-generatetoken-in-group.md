# Datasets GenerateTokenInGroup with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/GenerateToken`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Datasets GenerateTokenInGroup](https://learn.microsoft.com/en-us/rest/api/power-bi/embed-token/datasets-generate-token-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | The dataset ID |
| `accessLevel` | body | `object` | no | The required access level for embed token generation |
| `allowSaveAs` | body | `boolean` | no | Whether an embedded report can be saved as a new report. The default value is false. Only applies when you generate an embed token for report embedding. |
| `identities[]` | body | `array<object>` | no | A list of identities to use for row-level security rules |
| `lifetimeInMinutes` | body | `number` | no | The maximum lifetime of the token in minutes, starting from the time it was generated. Can be used to shorten the expiration time of a token, but not to extend it. The value must be a positive integer. Zero (0) is equivalent to null and will be ignored, resulting in the default expiration time. |
