# Get Split File URLs with Docsumo

Retrieves split-document file URLs from Docsumo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/mew/apikey/autosplit/files/:original_doc_id/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Get Split File URLs](https://support.docsumo.com/reference/get-split-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `original_doc_id` | path | `string` | yes | Original Docsumo document ID before split. |
