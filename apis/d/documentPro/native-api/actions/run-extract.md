# Run Extract with DocumentPro

Starts an extract job in DocumentPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/documents/:document_id/run_parser`
- **Base URL:** `https://api.documentpro.ai`
- **Official documentation:** [Run Extract](https://docs.documentpro.ai/docs/using-api/extract/document-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chunk_by_pages` | query | `number` | no | Optional page chunk size. |
| `detect_layout` | query | `boolean` | no | Whether to detect layout during parsing. |
| `detect_tables` | query | `boolean` | no | Whether to detect tables during parsing. |
| `document_id` | path | `string` | yes | The document_id to process. |
| `end_regex` | query | `string` | no | Optional end regex for splitting. |
| `page_ranges` | query | `string` | no | Optional page range selection, for example 1-3. |
| `query_model` | query | `string` | no | The query model to use for extraction. |
| `split_regex` | query | `string` | no | Optional split regex for parsing segments. |
| `start_regex` | query | `string` | no | Optional start regex for splitting. |
| `template_id` | query | `string` | yes | The workflow template_id to use for extraction. |
| `use_all_matches` | query | `boolean` | no | Whether to use all regex matches. |
| `use_ocr` | query | `boolean` | no | Whether to use OCR while parsing. |
