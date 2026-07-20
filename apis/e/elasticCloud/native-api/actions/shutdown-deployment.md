# Shut Down Deployment with Elastic Cloud

Shuts down a deployment in Elastic Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/deployments/:deployment_id/_shutdown`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Shut Down Deployment](https://www.elastic.co/docs/api/doc/cloud/operation/operation-shutdown-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deployment_id` | path | `string` | yes | Identifier for the deployment. |
| `hide` | query | `boolean` | no | Hide the deployment while shutting it down. Only applies to platform administrators. |
| `skip_snapshot` | query | `boolean` | no | Skip snapshots before shutting down the deployment resources. |
