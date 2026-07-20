# Extract With Model with ScrapFly

Retrieves extracted data from ScrapFly using AI extraction.

## Endpoint

- **Method:** `POST`
- **Path:** `/extraction`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Extract With Model](https://scrapfly.io/docs/extraction-api/automatic-ai)

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
| `extraction_model` | query | `string` | yes | Pretrained extraction model to apply to the provided document. |
