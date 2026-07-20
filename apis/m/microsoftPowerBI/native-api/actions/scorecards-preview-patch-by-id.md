# Patch By ID with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Patch By ID](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/patch-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `columnSettings[]` | body | `array<object>` | no | The display settings for columns on a scorecard |
| `createdTime` | body | `date` | no | The UTC time at creation |
| `datasetId` | body | `string` | no | The ID of the dataset associated with the scorecard |
| `description` | body | `string` | no | The scorecard description |
| `goals[]` | body | `array<object>` | no | The scorecard goals |
| `id` | body | `string` | no | The scorecard ID |
| `lastModifiedTime` | body | `date` | no | The UTC time at last modification |
| `name` | body | `string` | no | The scorecard name |
| `permissions` | body | `object` | no | The scorecard permissions |
| `provisioningStatus` | body | `object` | no | The provisioning status of the scorecard. |
| `reportId` | body | `string` | no | The ID of the internal report associated with the scorecard |
