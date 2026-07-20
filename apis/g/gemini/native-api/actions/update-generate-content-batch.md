# Update Generate Content Batch with Gemini

Updates a generate content batch in Gemini.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1beta/batches/:name`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Update Generate Content Batch](https://ai.google.dev/api/batch-api#method:-batches.updategeneratecontentbatch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Batch operation token without `batches/` prefix, for example `1234567890:updateGenerateContentBatch`. |
| `updateMask` | query | `string` | no | Comma-separated field mask for fields to update. |
| `model` | body | `string` | no | Model used by the batch. |
| `displayName` | body | `string` | no | Human-readable name for the batch. |
| `inputConfig` | body | `object` | no | Batch input configuration object. |
| `priority` | body | `string` | no | Optional batch scheduling priority. |
