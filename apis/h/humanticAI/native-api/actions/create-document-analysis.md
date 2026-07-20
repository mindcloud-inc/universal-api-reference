# Create Document Analysis with Humantic AI

## Endpoint

- **Method:** `POST`
- **Path:** `/user-profile/create`
- **Base URL:** `https://api.humantic.ai/v1`
- **Official documentation:** [Create Document Analysis](https://api.humantic.ai/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Unique identifier for the document analysis. Do not use values starting with `test`. |
| `document` | body | `file` | yes | PDF or DOCX document to analyze. |
| `doctype` | query | `string` | no | Set to `resume` when uploading a resume so Humantic can handle resume-specific context. |
| `stateless` | query | `boolean` | no | When true, Humantic does not save document input data. Applies only to text or document input. |
| `analysistype` | query | `string` | no | Use `talent` for English text or document input intended for hiring or talent assessment. |
