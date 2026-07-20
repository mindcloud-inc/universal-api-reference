# Create Batch with Voyage

Creates and executes a batch in Voyage.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batches`
- **Base URL:** `https://api.voyageai.com`
- **Official documentation:** [Create Batch](https://docs.voyageai.com/reference/create-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint` | body | `list` | yes | Voyage endpoint to run for every request in the batch. Accepted values: `0`, `1`, `2`. |
| `input_file_id` | body | `string` | yes | ID of the uploaded JSONL input file. |
| `completion_window` | body | `list` | yes | Time window for batch processing. Accepted values: `0`. |
| `request_params` | body | `object` | yes | Parameters applied to each request in the batch. |
