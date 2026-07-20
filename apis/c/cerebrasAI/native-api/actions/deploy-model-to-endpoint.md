# Deploy Model To Endpoint with Cerebras AI

Creates a model deployment to an endpoint in Cerebras AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/management/v1/endpoints/:endpointId:deployModel`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [Deploy Model To Endpoint](https://inference-docs.cerebras.ai/api-reference/customer_management_api/deploy-model-to-endpoint)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `endpointId` | path | `string` | yes |
| `model` | body | `string` | yes |
