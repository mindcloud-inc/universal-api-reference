# Create Batch Label with EasyPost

Creates a label for an existing batch in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/batches/:id/label`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Create Batch Label](https://docs.easypost.com/docs/batches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_format` | body | `string` | no | Optional label file format to create for the batch. |
| `id` | path | `string` | yes | EasyPost Batch ID, beginning with batch_. |
