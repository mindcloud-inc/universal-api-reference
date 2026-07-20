# Deploy All with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `pipelines/[:pipelineId]/deployAll`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Deploy All](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/deploy-all)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
| `sourceStageOrder` | body | `number` | yes | The numeric identifier of the pipeline deployment stage that the content should be deployed from. Development (0), Test (1), Production (2). |
| `isBackwardDeployment` | body | `boolean` | no | Whether the deployment will be from a later stage in the deployment pipeline, to an earlier one. The default value is false. |
| `newWorkspace` | body | `object` | no | The configuration details for creating a new workspace. Required when deploying to a stage that has no assigned workspaces. The deployment will fail if the new workspace configuration details aren't provided when required. |
| `note` | body | `string` | no | A note describing the deployment. |
| `options` | body | `object` | no | Options that control the behavior of the entire deployment |
| `updateAppSettings` | body | `date` | no | Update org app in the target workspace settings |
