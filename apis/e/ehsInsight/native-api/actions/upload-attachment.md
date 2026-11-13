# Upload Attachment with EHS Insight

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/attachment/add`
- **Base URL:** `https://{companyName}.ehsinsight.com/api`
- **Official documentation:** [Upload Attachment](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_attachmentapi_attachment_add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | no | File name including its extension, such as document.pdf. |
| `FileBytesBase64` | body | `string` | no | The file contents encoded as Base64, a text representation of the file's bytes. |
| `ContentType` | body | `string` | no | Optional media type, such as application/pdf. Inferred from the file name extension when omitted. |
| `RowUID` | body | `string` | no | Optional and not recommended for normal uploads. Supply only when migrating identical attachments between sandbox and production; otherwise let EHS Insight generate the identifier. |
