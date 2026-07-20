# Delete File with Text to pdf

Deletes a file from Text to PDF by file ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/execute/TEXT_TO_PDF_DELETE_FILE`
- **Base URL:** `https://backend.composio.dev/api/v3`
- **Official documentation:** [Delete File](https://docs.composio.dev/toolkits/text_to_pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arguments` | body | `object` | yes | Tool input arguments object. |
| `arguments.file_id` | body | `string` | yes | Unique file id to delete from temporary storage. |
