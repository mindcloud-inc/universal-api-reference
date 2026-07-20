# Create Embedding with CometAPI

Creates embeddings in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/embeddings`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Create Embedding](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Text or tokens to embed. |
| `model` | body | `string` | yes | Embedding model ID. |
