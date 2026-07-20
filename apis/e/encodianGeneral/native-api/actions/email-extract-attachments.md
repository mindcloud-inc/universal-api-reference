# Email Extract Attachments with Encodian - General

Extracts attachments from an email file in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/GetEmailAttachments`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Email Extract Attachments](https://support.encodian.com/hc/en-gb/articles/10531671561629)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileName` | body | `string` | yes | Email file name. |
| `fileContent` | body | `string` | yes | Base64-encoded email file content. |
| `getInlineAttachments` | body | `boolean` | yes | Whether to return inline attachments. |
