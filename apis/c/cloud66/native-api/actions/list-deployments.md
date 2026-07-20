# List Deployments with Cloud 66

Retrieves deployments from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:stack_id/deployments`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [List Deployments](https://developers.cloud66.com/v3/endpoints/deployments/#list-deployments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
