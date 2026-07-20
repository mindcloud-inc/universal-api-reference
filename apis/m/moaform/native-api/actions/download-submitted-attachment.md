# Download Submitted Attachment with Moaform

Retrieves a submitted attachment from Moaform.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/responses/:responseId/files/:fileId`
- **Base URL:** `https://api.moaform.com/v1`
- **Official documentation:** [Download Submitted Attachment](https://help.moaform.com/hc/en-us/articles/28408037219609-Downlodading-Submitted-Attachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | Unique ID of the form. |
| `response_id` | path | `string` | yes | Unique ID of the response. |
| `file_id` | path | `string` | yes | Unique ID of the submitted file. |
