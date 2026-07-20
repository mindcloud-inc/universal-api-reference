# Update Document with Paperless

## Endpoint

- **Method:** `PATCH`
- **Path:** `/documents/:id`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Update Document](https://developers.paperless.io/docs/api/dbf7092010e15-advanced-document-creation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Paperless document ID. |
| `name` | body | `string` | no | The new name for the document. |
| `state` | body | `string` | no | The target document state. |
| `settings` | body | `object` | no | The full settings object to apply to the document. |
| `reminder_settings` | body | `object` | no | Reminder configuration for the document. |
