# Batch Embed Contents with Gemini

Generates multiple content embeddings with Gemini.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/models/:model`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Batch Embed Contents](https://ai.google.dev/api/embeddings#method:-models.batchembedcontents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Required. Model endpoint token including suffix, for example gemini-embedding-001:batchEmbedContents. |
| `requests[]` | body | `array<object>` | yes | Required batch of EmbedContentRequest items. |
