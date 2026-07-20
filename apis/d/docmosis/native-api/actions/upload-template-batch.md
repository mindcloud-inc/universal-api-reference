# Upload Template Batch with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/uploadTemplateBatch`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Upload Template Batch](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=40)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateZip` | body | `file` | yes | Zip file containing the templates to upload. |
| `intoFolder` | body | `string` | no | Upload the templates into this environment folder path. |
| `userJobId` | body | `string` | no | Optional batch upload job identifier used for status and cancel calls. Maximum length: 40. |
| `devMode` | body | `boolean` | no | Upload templates in developer mode, allowing template errors. |
| `keepPrevOnFail` | body | `boolean` | no | Keep the previous template when a replacement upload fails in non-developer mode. |
| `fieldDelimPrefix` | body | `string` | no | Prefix delimiter for plain text merge fields. |
| `fieldDelimSuffix` | body | `string` | no | Suffix delimiter for plain text merge fields. |
| `normalizeTemplateName` | body | `boolean` | no | Normalize uploaded template names using Unicode NFC. |
