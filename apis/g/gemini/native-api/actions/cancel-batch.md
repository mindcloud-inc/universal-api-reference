# Cancel Batch with Gemini

Cancels a batch operation in Gemini.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/batches/:name`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Cancel Batch](https://ai.google.dev/api/batch-api#method:-batches.cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Batch operation token without `batches/` prefix, for example `1234567890:cancel`. |
