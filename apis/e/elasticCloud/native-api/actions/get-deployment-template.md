# Get Deployment Template with Elastic Cloud

Retrieves a deployment template from Elastic Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/deployments/templates/:template_id`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Get Deployment Template](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-deployment-template-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `region` | query | `string` | yes | Region of the deployment template. |
| `show_instance_configurations` | query | `boolean` | no | Return details for instance configurations referenced by the template. |
| `show_max_zones` | query | `boolean` | no | Populate max_zones in the instance configurations response. |
| `stack_version` | query | `string` | no | Adapt the returned template to the specified stack version. |
| `template_id` | path | `string` | yes | Identifier for the deployment template. |
