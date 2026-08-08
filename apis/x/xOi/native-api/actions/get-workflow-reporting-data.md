# Get Workflow Reporting Data with XOi

## Endpoint

- **Method:** `GET`
- **Path:** `https://api-jobs-external.xoi.io/prod/reporting-data/job/:jobId/workflow-job/:workflowJobId`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Get Workflow Reporting Data](https://integration-docs.xoi.io/guides/reporting/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `jobId` | path | `string` | yes |
| `workflowJobId` | path | `string` | yes |
