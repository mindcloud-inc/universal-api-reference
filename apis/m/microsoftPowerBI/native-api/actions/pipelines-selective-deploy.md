# Selective Deploy with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `pipelines/[:pipelineId]/deploy`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Selective Deploy](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/selective-deploy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
| `sourceStageOrder` | body | `number` | yes | The numeric identifier of the pipeline deployment stage that the content should be deployed from. Development (0), Test (1), Production (2). |
| `dashboards[]` | body | `array<object>` | no | A list of dashboards to be deployed |
| `dataflows[]` | body | `array<object>` | no | A list of dataflows to be deployed |
| `datamarts[]` | body | `array<object>` | no | A list of datamarts to be deployed |
| `datasets[]` | body | `array<object>` | no | A list of datasets to be deployed |
| `isBackwardDeployment` | body | `boolean` | no | Whether the deployment will be from a later stage in the deployment pipeline, to an earlier one. The default value is false. |
| `newWorkspace` | body | `object` | no | The configuration details for creating a new workspace. Required when deploying to a stage that has no assigned workspaces. The deployment will fail if the new workspace configuration details aren't provided when required. |
| `note` | body | `string` | no | A note describing the deployment. |
| `options` | body | `object` | no | Options that control the behavior of the entire deployment |
| `reports[]` | body | `array<object>` | no | A list of reports to be deployed |
| `updateAppSettings` | body | `date` | no | Update org app in the target workspace settings |
