# Create Document With Hidden Blocks with Paperless

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Create Document With Hidden Blocks](https://developers.paperless.io/docs/api/2ba41f7dfe8a3-visibility-of-blocks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | The workspace where the new document will be created. |
| `template_id` | body | `number` | yes | The template to use as the blueprint for the new document. |
| `name` | body | `string` | yes | The name of the new document. |
| `blocks` | body | `object` | yes | Block visibility overrides keyed by template block slug. |
