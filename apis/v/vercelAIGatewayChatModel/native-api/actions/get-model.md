# Get Model with Vercel AI Gateway Chat Model

Retrieves a specific model from Vercel AI Gateway.

## Endpoint

- **Method:** `GET`
- **Path:** `/models/:model`
- **Base URL:** `https://ai-gateway.vercel.sh/v1`
- **Official documentation:** [Get Model](https://vercel.com/docs/ai-gateway/openai-compat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Model identifier in creator/model format. |
