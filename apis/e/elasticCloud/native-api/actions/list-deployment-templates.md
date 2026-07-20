# List Deployment Templates with Elastic Cloud

Retrieves deployment templates from Elastic Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/deployments/templates`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [List Deployment Templates](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-deployment-templates-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `region` | query | `string` | yes | Region of the deployment templates. |
| `metadata` | query | `string` | no | Optional metadata filter in key:value form. |
| `show_instance_configurations` | query | `boolean` | no | Return details for each instance configuration referenced by the template. |
| `show_max_zones` | query | `boolean` | no | Populate max_zones in instance configurations when instance configurations are shown. |
| `stack_version` | query | `string` | no | Adapt returned templates to the given stack version. |
| `hide_deprecated` | query | `boolean` | no | Exclude templates flagged as deprecated. |
