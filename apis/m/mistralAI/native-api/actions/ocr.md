# OCR with Mistral AI

Creates OCR results for a document in Mistral AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ocr`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [OCR](https://docs.mistral.ai/api/endpoint/ocr#operation-ocr_v1_ocr_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | OCR model ID. |
| `document` | body | `object` | yes | Document source object to run OCR on. |
| `id` | body | `string` | no | Optional client identifier for the OCR request. |
| `pages[]` | body | `array<number>` | no | Specific page numbers to process. |
| `include_image_base64` | body | `boolean` | no | Include extracted image content in the response. |
| `image_limit` | body | `number` | no | Maximum number of images to extract. |
| `image_min_size` | body | `number` | no | Minimum image size threshold for extraction. |
| `bbox_annotation_format` | body | `object` | no | Structured output format for extracted bounding boxes or images. |
| `document_annotation_format` | body | `object` | no | Structured output format for the full document. |
| `document_annotation_prompt` | body | `string` | no | Prompt that guides document-level structured extraction. |
| `table_format` | body | `string` | no | Table output format such as markdown or html. |
| `extract_header` | body | `boolean` | no | Whether to extract document header regions. |
| `extract_footer` | body | `boolean` | no | Whether to extract document footer regions. |
