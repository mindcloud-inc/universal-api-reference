# Embed Content with Google AI Studio

Generates text embeddings with a Gemini model in Google AI Studio.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/models/:model`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Embed Content](https://ai.google.dev/api/embeddings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Required. Model endpoint token including suffix, for example `gemini-embedding-001:embedContent`. |
| `content` | body | `object` | yes | Required content object to embed. |
| `taskType` | body | `string` | no | Optional embedding task type. |
| `title` | body | `string` | no | Optional title used for retrieval document embeddings. |
| `outputDimensionality` | body | `number` | no | Optional reduced embedding dimension. |
