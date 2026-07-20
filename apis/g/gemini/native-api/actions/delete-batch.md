# Delete Batch with Gemini

Deletes a batch operation from Gemini.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v1beta/batches/:name`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Delete Batch](https://ai.google.dev/api/batch-api#method:-batches.delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Batch ID segment (without `batches/` prefix), for example `1234567890`. |
