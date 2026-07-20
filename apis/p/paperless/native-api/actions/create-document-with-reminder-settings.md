# Create Document With Reminder Settings with Paperless

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Create Document With Reminder Settings](https://developers.paperless.io/docs/api/dbf7092010e15-advanced-document-creation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | The workspace where the new document will be created. |
| `template_id` | body | `number` | yes | The template to use as the blueprint for the new document. |
| `name` | body | `string` | yes | The name of the new document. |
| `reminder_settings` | body | `object` | yes | Reminder configuration for the new document. |
