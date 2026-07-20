# Create Vector Store with Open AI

Creates a vector store in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/vector_stores`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Create Vector Store](https://developers.openai.com/api/reference/resources/vector_stores/methods/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional name for the vector store. |
| `file_ids[]` | body | `array<string>` | no | Optional file IDs to attach at creation. |
