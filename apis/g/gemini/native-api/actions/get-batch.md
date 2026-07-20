# Get Batch with Gemini

Retrieves a batch operation from Gemini.

## Endpoint

- **Method:** `GET`
- **Path:** `v1beta/batches/:name`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Get Batch](https://ai.google.dev/api/batch-api#method:-batches.get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Batch ID segment (without `batches/` prefix), for example `1234567890`. |
