# Show Model Details with Ollama

Retrieves model details from Ollama.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/show`
- **Base URL:** `https://ollama.com`
- **Official documentation:** [Show Model Details](https://docs.ollama.com/api-reference/show-model-details)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `verbose` | body | `boolean` | no |
