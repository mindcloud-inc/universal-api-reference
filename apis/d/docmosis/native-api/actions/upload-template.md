# Upload Template with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/uploadTemplate`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Upload Template](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=29)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateFile` | body | `file` | yes | The DOCX template file to upload. |
| `templateName` | body | `string` | no | Optional overriding template path and file name. |
| `templateDescription` | body | `string` | no | Optional description stored with the uploaded template. |
| `devMode` | body | `boolean` | no | Whether to upload in developer mode. |
| `keepPrevOnFail` | body | `boolean` | no | Whether to keep the previous template when a non-dev upload fails. |
