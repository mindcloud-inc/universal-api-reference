# Create Pipeline with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `pipelines`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Create Pipeline](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/create-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | yes | The display name for the new deployment pipeline |
| `description` | body | `string` | no | The description for the new deployment pipeline |
