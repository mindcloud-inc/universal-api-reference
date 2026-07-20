# Create Document From Template with Paperless

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Create Document From Template](https://developers.paperless.io/docs/api/95ee69b4b848f-using-templates-with-the-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | The workspace where the new document will be created. |
| `template_id` | body | `number` | yes | The template to use as the blueprint for the new document. |
| `name` | body | `string` | yes | The name of the new document. |
