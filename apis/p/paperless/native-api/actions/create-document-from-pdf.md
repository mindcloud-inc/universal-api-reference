# Create Document From PDF with Paperless

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Create Document From PDF](https://developers.paperless.io/docs/api/bb191806bdd25-create-a-document-from-a-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | The workspace where the new document will be created. |
| `pdf` | body | `string` | yes | The signed_id of the uploaded PDF blob. |
| `name` | body | `string` | yes | The name of the new document. |
