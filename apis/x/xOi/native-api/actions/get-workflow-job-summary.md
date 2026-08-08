# Get Workflow Job Summary with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-jobs-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Get Workflow Job Summary](https://integration-docs.xoi.io/schemas/jobs/#getjobsummaryinput)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.jobId` | body | `string` | yes |
| `variables.workflowJobId` | body | `string` | yes |
| `variables.includeAllSteps` | body | `boolean` | no |
