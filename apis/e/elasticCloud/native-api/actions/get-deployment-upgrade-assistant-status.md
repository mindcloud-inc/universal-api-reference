# Get Deployment Upgrade Assistant Status with Elastic Cloud

Retrieves deployment upgrade assistant status from Elastic Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/deployments/:deployment_id/upgrade_assistant/status`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Get Deployment Upgrade Assistant Status](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-deployment-upgrade-assistant-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deployment_id` | path | `string` | yes | Identifier for the deployment. |
| `target_version` | query | `string` | no | Optional target version to include in the upgrade assistant request. |
