# List Model Versions with Cerebras AI

Retrieves model versions from Cerebras AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/management/v1/orgs/:orgName/models/:modelArchId/versions`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [List Model Versions](https://inference-docs.cerebras.ai/api-reference/customer_management_api/list-model-versions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orgName` | path | `string` | yes |
| `modelArchId` | path | `string` | yes |
