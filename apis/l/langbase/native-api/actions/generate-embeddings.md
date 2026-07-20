# Generate Embeddings with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/embed`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Generate Embeddings](https://langbase.com/docs/api-reference/embed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chunks[]` | body | `array<string>` | yes | Array of text chunks to embed. |
