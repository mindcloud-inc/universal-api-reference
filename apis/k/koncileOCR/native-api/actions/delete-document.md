# Delete Document with Koncile OCR

## Endpoint

- **Method:** `DELETE`
- **Path:** `/delete_doc`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Delete Document](https://docs.koncile.ai/api-setup/documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delete_file` | query | `boolean` | no | Also delete the underlying stored file when true. |
| `doc_id` | query | `number` | yes | Delete this document ID from Koncile. |
