# Post with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/scorecards`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Post](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `name` | body | `string` | yes | The scorecard name |
| `description` | body | `string` | no | Optional. The scorecard description. |
| `sensitivityLabelId` | body | `string` | no | Optional. The GUID of a sensitivity label. If you don't want to select a sensitivity label, use a null or empty GUID (00000000-0000-0000-0000-000000000000). If default labels are enabled and/or enforced, they will be applied on the scorecard and dataset. |
