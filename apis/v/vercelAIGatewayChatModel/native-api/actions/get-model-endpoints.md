# Get Model Endpoints with Vercel AI Gateway Chat Model

Retrieves provider endpoints for a specific Vercel AI Gateway model.

## Endpoint

- **Method:** `GET`
- **Path:** `/models/:creator/:model/endpoints`
- **Base URL:** `https://ai-gateway.vercel.sh/v1`
- **Official documentation:** [Get Model Endpoints](https://vercel.com/docs/ai-gateway/models-and-providers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `creator` | path | `string` | yes | Model creator slug, such as google or openai. |
| `model` | path | `string` | yes | Model slug without the creator prefix. |
