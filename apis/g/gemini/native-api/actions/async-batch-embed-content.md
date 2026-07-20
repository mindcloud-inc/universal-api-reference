# Async Batch Embed Content with Gemini

Enqueues a batch embed content job in Gemini.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/models/:model`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Async Batch Embed Content](https://ai.google.dev/api/batch-api#method:-models.asyncbatchembedcontent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Required. Model endpoint token including suffix, for example gemini-embedding-001:asyncBatchEmbedContent. |
| `batch` | body | `object` | yes | Required embed batch payload. |
