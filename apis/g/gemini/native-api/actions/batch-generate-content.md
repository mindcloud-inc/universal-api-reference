# Batch Generate Content with Gemini

Enqueues a batch generate content job in Gemini.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/models/:model`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Batch Generate Content](https://ai.google.dev/api/batch-api#method:-models.batchgeneratecontent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Required. Model endpoint token including suffix, for example gemini-2.5-flash:batchGenerateContent. |
| `batch` | body | `object` | yes | Required generate-content batch payload with `model`, `displayName`, and `inputConfig` (either fileName or inline requests). |
