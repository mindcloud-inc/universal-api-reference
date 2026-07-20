# Set Deployment Tags with Elastic Cloud

Updates deployment tags in Elastic Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/deployments/:deployment_id/tags`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Set Deployment Tags](https://www.elastic.co/docs/api/doc/cloud/operation/operation-set-deployment-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | The tags to set on the deployment. |
| `deployment_id` | path | `string` | yes | Identifier for the deployment. |
