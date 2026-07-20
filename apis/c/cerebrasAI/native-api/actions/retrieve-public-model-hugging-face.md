# Retrieve Public Model (HuggingFace) with Cerebras AI

Retrieves a HuggingFace-formatted public model from Cerebras AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v1/models/:modelId`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [Retrieve Public Model (HuggingFace)](https://inference-docs.cerebras.ai/api-reference/models/public-models)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `modelId` | path | `string` | yes |
