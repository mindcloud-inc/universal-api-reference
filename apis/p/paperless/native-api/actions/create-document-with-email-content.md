# Create Document With Email Content with Paperless

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Create Document With Email Content](https://developers.paperless.io/docs/api/ec1d64419e849-setting-the-e-mail-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | The workspace where the new document will be created. |
| `name` | body | `string` | yes | The name of the new document. |
| `settings` | body | `object` | yes | Document settings, including mail subject, content, and signature. |
