# Create Embedding with Groq

Creates an embedding in Groq.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/v1/embeddings`
- **Base URL:** `https://api.groq.com`
- **Official documentation:** [Create Embedding](https://console.groq.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | The Groq embedding model identifier to use. |
| `input` | body | `string` | yes | Text input to embed. Groq also supports array input, which is not yet fully modeled in this scaffold. |
| `encoding_format` | body | `list` | no | Embedding output format. |
| `user` | body | `string` | no | — |
