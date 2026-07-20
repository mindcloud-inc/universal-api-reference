# Update Deployment with Elastic Cloud

Updates an existing deployment in Elastic Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/deployments/:deployment_id`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Update Deployment](https://www.elastic.co/docs/api/doc/cloud/operation/operation-update-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | The deployment definition to apply. |
| `deployment_id` | path | `string` | yes | Identifier for the deployment. |
| `hide_pruned_orphans` | query | `boolean` | no | Hide orphaned resources that were shut down when pruning is enabled. |
| `skip_snapshot` | query | `boolean` | no | Skip snapshots before shutting down orphaned resources when pruning is enabled. |
| `validate_only` | query | `boolean` | no | Validate the deployment update without applying it. |
| `version` | query | `string` | no | Resource version to use for conflict checks during the update. |
