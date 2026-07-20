# Create Deployment with Elastic Cloud

Creates a new deployment in Elastic Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/deployments`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Create Deployment](https://www.elastic.co/docs/api/doc/cloud/operation/operation-create-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | The deployment definition to create. |
| `request_id` | query | `string` | no | Optional idempotency token for deployment creation requests. |
| `template_id` | query | `string` | no | Optional deployment template to use when creating the deployment. |
| `validate_only` | query | `boolean` | no | Validate the deployment definition without creating the deployment. |
