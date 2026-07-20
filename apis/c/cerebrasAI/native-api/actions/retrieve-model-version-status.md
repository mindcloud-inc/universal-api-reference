# Retrieve Model Version Status with Cerebras AI

Retrieves model version status from Cerebras AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/management/v1/orgs/:orgName/models/:modelArchId/versions/:versionId`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [Retrieve Model Version Status](https://inference-docs.cerebras.ai/api-reference/customer_management_api/retrieve-model-version-status)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orgName` | path | `string` | yes |
| `modelArchId` | path | `string` | yes |
| `versionId` | path | `string` | yes |
