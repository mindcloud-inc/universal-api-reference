# Delete Model Version with Cerebras AI

Deletes a model version from Cerebras AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/management/v1/orgs/:orgName/models/:modelArchId/versions/:versionId`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [Delete Model Version](https://inference-docs.cerebras.ai/api-reference/customer_management_api/delete-model-version)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orgName` | path | `string` | yes |
| `modelArchId` | path | `string` | yes |
| `versionId` | path | `string` | yes |
