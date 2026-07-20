# Create Blob For Attachment with Paperless

## Endpoint

- **Method:** `POST`
- **Path:** `/blobs`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Create Blob For Attachment](https://developers.paperless.io/docs/api/bb191806bdd25-create-a-document-from-a-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `byte_size` | body | `number` | yes | The size of the blob in bytes. |
| `checksum` | body | `string` | yes | The content checksum expected by Paperless. |
| `content_type` | body | `string` | yes | The blob MIME type. |
| `filename` | body | `string` | yes | The filename to register for the blob. |
