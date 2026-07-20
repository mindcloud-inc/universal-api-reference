# Extract With Prompt with ScrapFly

Retrieves extracted data from ScrapFly using an LLM prompt.

## Endpoint

- **Method:** `POST`
- **Path:** `/extraction`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Extract With Prompt](https://scrapfly.io/docs/extraction-api/llm-prompt)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/html` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Raw document content to extract from. |
| `content_type` | query | `string` | yes | Content type of the raw body, such as text/html or application/json. |
| `extraction_prompt` | query | `string` | yes | LLM instruction describing what to extract from the provided document. |
