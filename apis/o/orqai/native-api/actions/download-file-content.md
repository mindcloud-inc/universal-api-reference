# Download File Content with Orq.ai

Retrieves a presigned file download URL from Orq.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/files/[:file_id_or_path]/content`
- **Base URL:** `https://api.orq.ai`
- **Official documentation:** [Download File Content](https://docs.orq.ai/reference/files/download-file-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id_or_path` | path | `string` | yes | File ID or Path from the Orq.ai path parameter. |
