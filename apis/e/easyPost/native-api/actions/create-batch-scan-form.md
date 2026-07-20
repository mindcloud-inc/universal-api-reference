# Create Batch Scan Form with EasyPost

Creates a scan form for an existing batch in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/batches/:id/scan_form`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Create Batch Scan Form](https://docs.easypost.com/docs/batches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Batch ID, beginning with batch_. |
