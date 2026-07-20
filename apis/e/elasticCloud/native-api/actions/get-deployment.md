# Get Deployment with Elastic Cloud

Retrieves a deployment from Elastic Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/deployments/:deployment_id`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Get Deployment](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clear_transient` | query | `boolean` | no | Remove transient sections from child resources in the response. |
| `convert_legacy_plans` | query | `boolean` | no | Convert legacy plans to the 2.x format in the response. |
| `deployment_id` | path | `string` | yes | Identifier for the deployment. |
| `enrich_with_template` | query | `boolean` | no | Enrich plan data with missing elements from the deployment template. |
| `force_all_plan_history` | query | `boolean` | no | Return the full plan history even when it is very large. |
| `show_instance_configurations` | query | `boolean` | no | Return details for each instance configuration referenced by the deployment. |
| `show_instance_metrics` | query | `boolean` | no | Include resource instance metrics in the response. |
| `show_metadata` | query | `boolean` | no | Include full cluster metadata in the response. |
| `show_plan_defaults` | query | `boolean` | no | Show values that remain at their default values in the plan response. |
| `show_plan_history` | query | `boolean` | no | Include plan history with current and pending plan information. |
| `show_plan_logs` | query | `boolean` | no | Include attempt logs with current and pending plan information. |
| `show_plans` | query | `boolean` | no | Include current and pending plan information in the response. |
| `show_security` | query | `boolean` | no | Include Elasticsearch security information in the response. |
| `show_settings` | query | `boolean` | no | Include cluster settings in the response. |
| `show_system_alerts` | query | `number` | no | Number of system alerts to include in the response. |
