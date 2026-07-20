# Restore Deployment with Elastic Cloud

Restores a shutdown deployment in Elastic Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/deployments/:deployment_id/_restore`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Restore Deployment](https://www.elastic.co/docs/api/doc/cloud/operation/operation-restore-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deployment_id` | path | `string` | yes | Identifier for the deployment. |
| `restore_snapshot` | query | `boolean` | no | Restore a snapshot for supported resources when restoring the deployment. |
