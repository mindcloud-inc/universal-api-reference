# Update Model Version Aliases with Cerebras AI

Updates model version aliases in Cerebras AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/management/v1/orgs/:orgName/models/:modelArchId/versions/:versionId`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [Update Model Version Aliases](https://inference-docs.cerebras.ai/api-reference/customer_management_api/update-model-version-aliases)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orgName` | path | `string` | yes |
| `modelArchId` | path | `string` | yes |
| `versionId` | path | `string` | yes |
| `version_aliases[]` | body | `array<string>` | yes |
