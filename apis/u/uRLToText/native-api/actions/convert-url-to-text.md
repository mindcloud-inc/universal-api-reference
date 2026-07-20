# Convert URL to Text with URL to Text

Retrieves extracted webpage or YouTube content from URL to Text.

## Endpoint

- **Method:** `POST`
- **Path:** `/urltotext/`
- **Base URL:** `https://urltotext.com/api/v1`
- **Official documentation:** [Convert URL to Text](https://urltotext.com/documentation/api-docs/url-to-text/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The webpage or YouTube URL to convert. |
| `output_format` | body | `list<string>` | no | The format to return. URLtoText supports text, markdown, and html. Accepted values: `0`, `1`, `2`. |
| `extract_main_content` | body | `boolean` | no | Use URLtoText's AI extraction to attempt to return only the main content. |
| `render_javascript` | body | `boolean` | no | Render JavaScript before extracting content. |
| `residential_proxy` | body | `boolean` | no | Use a residential proxy for the request. Only one proxy option should be enabled at a time. |
| `stealth_proxy` | body | `boolean` | no | Use URLtoText's premium residential IP pool. Requires JavaScript rendering. |
| `ai_prompt` | body | `string` | no | Optional AI prompt to process or modify the extracted content. |
| `end_of_article` | body | `string` | no | Optional text marker where extraction should stop. |
| `wait_for_js` | body | `number` | no | Milliseconds to wait for JavaScript to finish loading before extraction. |
| `extract_css_selector` | body | `string` | no | One or more CSS selectors separated by commas. If omitted or unmatched, the whole page is processed. |
