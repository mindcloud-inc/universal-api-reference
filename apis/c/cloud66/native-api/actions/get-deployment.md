# Get Deployment with Cloud 66

Retrieves a deployment from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:stack_id/deployments/:deployment_id`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Get Deployment](https://developers.cloud66.com/v3/endpoints/deployments/#get-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
| `deployment_id` | path | `number` | yes | The deployment ID |
