# Run Workflow with Comfy.ICU

Creates a new workflow run in Comfy.ICU.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/workflows/:workflow_id/runs`
- **Base URL:** `https://comfy.icu`
- **Official documentation:** [Run Workflow](https://comfy.icu/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | Comfy.ICU workflow ID from the workflow page or API code snippet. |
| `prompt` | body | `string` | yes | ComfyUI API-format workflow JSON prompt. Paste the full prompt JSON from Comfy.ICU's View API code output. |
| `files` | body | `string` | no | Optional JSON object mapping ComfyUI destination paths to public file URLs for inputs, models, LoRAs, or embeddings. |
| `webhook` | body | `string` | no | Optional public endpoint Comfy.ICU should call with run status updates. |
| `accelerator` | body | `string` | no | Optional GPU accelerator to use for the workflow run. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
