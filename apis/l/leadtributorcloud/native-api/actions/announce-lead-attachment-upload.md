# Announce Lead Attachment Upload with leadtributor.cloud

Creates an attachment upload request for a lead in leadtributor.cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/:leadId/attachments`
- **Base URL:** `https://api.leadtributor.cloud`
- **Official documentation:** [Announce Lead Attachment Upload](https://developer.leadtributor.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contentType` | body | `string` | yes | MIME type of the attachment to upload. |
| `filename` | body | `string` | yes | Filename to announce for upload. |
| `leadId` | path | `string` | yes | ID of the lead to attach a file to. |
