# Email Extract Attachments with Encodian

Retrieves email attachments from Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/GetEmailAttachments`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Email Extract Attachments](https://support.encodian.com/hc/en-gb/articles/10531671561629)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | The filename, including file extension, of the source email file. |
| `fileContent` | body | `string` | yes | A Base64 encoded representation of the email file to be processed. |
| `getInlineAttachments` | body | `boolean` | no | Set whether to extract inline attachments. |
