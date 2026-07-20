# Get Pipeline Stage Artifacts with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `pipelines/[:pipelineId]/stages/[:stageOrder]/artifacts`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Pipeline Stage Artifacts](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipeline-stage-artifacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
| `stageOrder` | path | `number` | yes | The deployment pipeline stage order. Development (0), Test (1), Production (2). |
