# Redeploy Stack with Cloud 66

Redeploys a stack in your Cloud 66 account.

## Endpoint

- **Method:** `POST`
- **Path:** `/stacks/:stack_id/deployments`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Redeploy Stack](https://developers.cloud66.com/v3/endpoints/deployments/#redeploy-stack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID. |
| `git_ref` | query | `string` | no | Git reference to redeploy for non-docker stacks. |
| `services` | query | `string` | no | Docker service:image_tag pairs to deploy. |
| `deployment_profile` | query | `string` | no | Deployment profile name. |
| `user_reference` | query | `string` | no | Metadata reference to attach to the stack action. |
