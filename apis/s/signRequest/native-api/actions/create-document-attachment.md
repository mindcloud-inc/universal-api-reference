# Create Document Attachment with SignRequest

## Endpoint

- **Method:** `POST`
- **Path:** `/document-attachments/`
- **Base URL:** `https://signrequest.com/api/v1`
- **Official documentation:** [Create Document Attachment](https://signrequest.com/api/v1/docs/#operation/document-attachments_create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `document` | body | `string` | yes |
| `file_from_url` | body | `string` | no |
| `file_from_content` | body | `string` | no |
| `file_from_content_name` | body | `string` | no |
| `name` | body | `string` | no |
