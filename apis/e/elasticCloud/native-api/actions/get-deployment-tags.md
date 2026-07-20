# Get Deployment Tags with Elastic Cloud

Retrieves deployment tags from Elastic Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/deployments/:deployment_id/tags`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Get Deployment Tags](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-deployment-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deployment_id` | path | `string` | yes | Identifier for the deployment. |
