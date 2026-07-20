# Create Push Dataset in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/datasets`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Create Push Dataset in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-post-dataset-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `name` | body | `string` | yes | The push dataset name. |
| `tables[]` | body | `array<object>` | yes | Array of table definitions for the push dataset. |
| `defaultRetentionPolicy` | query | `list` | no | Optional retention policy for the push dataset. |
