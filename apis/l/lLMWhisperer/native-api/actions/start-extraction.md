# Start Extraction From URL with LLMWhisperer

Starts a document extraction job in LLMWhisperer from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/whisper`
- **Base URL:** `https://llmwhisperer-api.us-central.unstract.com/api/v2`
- **Official documentation:** [Start Extraction From URL](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_text_extraction_api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Publicly accessible URL of the document to extract. This action uses the documented URL submission path for /whisper. |
| `mode` | query | `string` | no | Processing mode such as native_text, low_cost, high_quality, form, or table. |
| `output_mode` | query | `string` | no | Choose layout_preserving or text output. |
| `pages_to_extract` | query | `string` | no | Comma/range page selector such as 1-5,7,21-. |
| `page_seperator` | query | `string` | no | String inserted between extracted pages. |
| `line_splitter_tolerance` | query | `number` | no | Baseline tolerance factor for line splitting. |
| `horizontal_stretch_factor` | query | `number` | no | Horizontal stretch factor for difficult layouts. |
| `line_splitter_strategy` | query | `string` | no | Advanced line splitter strategy. |
| `median_filter_size` | query | `number` | no | Median filter size for low_cost mode noise reduction. |
| `gaussian_blur_radius` | query | `number` | no | Gaussian blur radius for low_cost mode noise reduction. |
| `mark_vertical_lines` | query | `boolean` | no | Preserve vertical lines when supported. |
| `mark_horizontal_lines` | query | `boolean` | no | Preserve horizontal lines when supported. |
| `lang` | query | `string` | no | OCR language hint. |
| `tag` | query | `string` | no | Audit tag used in usage reports. |
| `file_name` | query | `string` | no | Audit file name value stored with the extraction run. |
| `use_webhook` | query | `string` | no | Previously registered webhook name to notify after processing completes. |
| `webhook_metadata` | query | `string` | no | Metadata string sent verbatim to the webhook callback. |
| `add_line_nos` | query | `boolean` | no | Include line numbers and save highlight metadata. |
| `allow_rotated_text` | query | `boolean` | no | Preserve rotated or angled text when supported. |
