# Create Batch with Open AI

Creates a batch in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/batches`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Create Batch](https://developers.openai.com/api/reference/resources/batches/methods/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input_file_id` | body | `string` | yes | ID of the uploaded JSONL input file. |
| `endpoint` | body | `list` | yes | API endpoint to process for each line item. |
| `completion_window` | body | `list` | yes | Allowed time window for batch completion. |
