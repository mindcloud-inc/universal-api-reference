# Download Attachment with ActivityInfo

Downloads an attachment from an ActivityInfo record.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/form/:formId/record/:recordId/field/:fieldId/blob/:blobId/:filename`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [Download Attachment](https://www.activityinfo.org/support/docs/api/reference/getAttachment.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ActivityInfo form ID. |
| `recordId` | path | `string` | yes | ActivityInfo record ID. |
| `fieldId` | path | `string` | yes | ActivityInfo field ID. |
| `blobId` | path | `string` | yes | ActivityInfo attachment blob ID. |
| `filename` | path | `string` | yes | Filename suffix used by ActivityInfo for browser download behavior. |
