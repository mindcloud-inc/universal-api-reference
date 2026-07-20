# Create Advanced Document with Paperless

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Create Advanced Document](https://developers.paperless.io/docs/api/dbf7092010e15-advanced-document-creation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | The workspace where the new document will be created. |
| `name` | body | `string` | yes | The name of the new document. |
| `description` | body | `string` | no | The description of the new document. |
| `participants` | body | `object` | no | Participant attributes keyed by participant slot name. |
| `settings` | body | `object` | no | Document settings to apply when creating the document. |
| `reminder_settings` | body | `object` | no | Reminder configuration for the new document. |
