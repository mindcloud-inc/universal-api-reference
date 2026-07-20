# Create Workflow Dispatch Event with GitHub

Triggers a GitHub Actions workflow run.

## Endpoint

- **Method:** `POST`
- **Path:** `/repos/:owner/:repo/actions/workflows/:workflow_id/dispatches`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Create Workflow Dispatch Event](https://docs.github.com/en/rest/actions/workflows#create-a-workflow-dispatch-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `workflow_id` | path | `string` | yes | The workflow ID or workflow file name. |
| `ref` | body | `string` | yes | The git reference for the workflow. The reference can be a branch or tag name. |
| `inputs` | body | `object` | no | Input keys and values configured in the workflow file. |
| `return_run_details` | body | `boolean` | no | Whether the response should include the workflow run ID and URLs. |
