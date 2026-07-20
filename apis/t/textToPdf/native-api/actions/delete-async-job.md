# Delete Async Job with Text to pdf

Deletes an asynchronous job from Text to PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/execute/TEXT_TO_PDF_DELETE_ASYNC_JOB`
- **Base URL:** `https://backend.composio.dev/api/v3`
- **Official documentation:** [Delete Async Job](https://docs.composio.dev/toolkits/text_to_pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arguments` | body | `object` | yes | Tool input arguments object. |
| `arguments.job_id` | body | `string` | yes | Unique asynchronous conversion job id to delete. |
