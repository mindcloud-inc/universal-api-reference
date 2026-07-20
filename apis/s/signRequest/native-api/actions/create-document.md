# Create Document with SignRequest

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/`
- **Base URL:** `https://signrequest.com/api/v1`
- **Official documentation:** [Create Document](https://signrequest.com/api/v1/docs/#operation/documents_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_from_url` | body | `string` | no | Publicly accessible URL of the document to download Maximum length: 2100. |
| `name` | body | `string` | no | Defaults to filename, including extension Maximum length: 255. |
| `file_from_content` | body | `string` | no | Base64 encoded document content |
| `file_from_content_name` | body | `string` | no | Filename, including extension, required when using file_from_content |
| `template` | body | `string` | no | Template URI to use for the document |
| `external_id` | body | `string` | no | ID used to reference document in external system Maximum length: 255. |
| `events_callback_url` | body | `string` | no | URL that should receive document event callbacks Maximum length: 2100. |
| `auto_delete_days` | body | `number` | no | Automatically delete finished documents after this many days |
| `auto_expire_days` | body | `number` | no | Automatically expire unfinished documents after this many days |
| `frontend_id` | body | `string` | no | Shared secret used with the SignRequest JS client to grant document access Maximum length: 255. |
| `file_from_sf` | body | `object` | no | Salesforce file source configuration |
| `prefill_tags[]` | body | `array<object>` | no | Prefill signer input data for templates |
| `integrations[]` | body | `array<object>` | no | Integration-specific document metadata |
