# Render Documents with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/render`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Render Documents](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=15)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateName` | body | `string` | yes | Name of the template to render. The template must already exist in Docmosis. |
| `outputName` | body | `string` | yes | Filename for the rendered document output. The extension can imply the format when Output Format is omitted. |
| `data` | body | `object` | no | Structured JSON data merged into the template. |
| `streamResultInResponse` | body | `boolean` | no | When true, base64-encodes the streamed result into the JSON response body. |
| `outputFormat` | body | `string` | no | Optional output format. Valid options are PDF, DOCX, ODT, or TXT. |
| `storeTo` | body | `string` | no | Optional destination for the rendered output such as stream, mailto, or s3. Defaults to streaming the result back. |
| `requestId` | body | `string` | no | Optional caller-provided identifier echoed back in the response. |
| `tags` | body | `string` | no | Semicolon-separated tags to record against this render for later reporting. |
| `devMode` | body | `string` | no | If set to y, yes, or true, render in development mode instead of failing hard on template/data issues. |
