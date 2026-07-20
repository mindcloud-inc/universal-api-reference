# Retrieve Public Model (Generic Format) with Cerebras AI

Retrieves a public model from Cerebras AI by format.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v1/models/:modelId`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [Retrieve Public Model (Generic Format)](https://inference-docs.cerebras.ai/api-reference/models/public-models)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `modelId` | path | `string` | yes |
| `format` | query | `string` | no |
