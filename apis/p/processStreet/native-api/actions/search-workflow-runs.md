# Search Workflow Runs with Process Street

## Endpoint

- **Method:** `GET`
- **Path:** `/workflow-runs`
- **Base URL:** `https://public-api.process.st/api/v1.1`
- **Official documentation:** [Search Workflow Runs](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/GET/workflow-runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | query | `string` | no | The ID of the workflow. |
| `name` | query | `string` | no | Filter workflow runs by partial name. |
| `status` | query | `string` | no | Filter by one or more workflow run statuses. Send multiple values as a string separated by `,`. |
