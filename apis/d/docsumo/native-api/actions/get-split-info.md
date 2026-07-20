# Get Split Info with Docsumo

Retrieves split-document metadata and file options from Docsumo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/mew/apikey/autosplit/info/:original_doc_id/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Get Split Info](https://support.docsumo.com/reference/get-split-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `original_doc_id` | path | `string` | yes | Original Docsumo document ID before split. |
