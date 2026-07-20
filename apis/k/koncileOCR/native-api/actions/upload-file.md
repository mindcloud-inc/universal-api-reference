# Upload File with Koncile OCR

## Endpoint

- **Method:** `POST`
- **Path:** `/upload_file`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Upload File](https://docs.koncile.ai/api-setup/file-uploading)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doc_id` | body | `number` | no | Complete an existing document by document ID. |
| `files` | body | `file` | yes | One file to upload for extraction. Koncile accepts PDF, PNG, and JPEG uploads on the files field. |
| `folder_id` | body | `number` | no | Store the uploaded document in this folder. |
| `metadata` | body | `string` | no | A JSON string with contextual extraction hints. |
| `template_id` | body | `number` | no | Extract data with this template. |
