# Create Document With Redirect URL with Paperless

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Create Document With Redirect URL](https://developers.paperless.io/docs/api/529adde2f023e-create-and-send-your-first-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | The workspace where the new document will be created. |
| `template_id` | body | `number` | yes | The template to use as the blueprint for the new document. |
| `name` | body | `string` | yes | The name of the new document. |
| `participant_completed_redirect_url` | body | `string` | yes | The URL where participants are redirected after completion. |
