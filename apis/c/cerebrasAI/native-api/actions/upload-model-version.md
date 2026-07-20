# Upload Model Version with Cerebras AI

Creates a model version in Cerebras AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/management/v1/orgs/:orgName/models:upload`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [Upload Model Version](https://inference-docs.cerebras.ai/api-reference/customer_management_api/upload-model-version)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orgName` | path | `string` | yes |
| `model_arch_id` | body | `string` | yes |
| `model.weight_uri` | body | `string` | yes |
