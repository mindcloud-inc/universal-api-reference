# Complete Upload with AnyDB

Completes an attachment upload in AnyDB.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/integrations/ext/completeupload`
- **Base URL:** `https://app.anydb.com`
- **Official documentation:** [Complete Upload](https://www.anydb.com/openapi/spec.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filesize` | body | `number` | yes | The uploaded file size in bytes. |
| `teamid` | body | `string` | yes | The AnyDB team ID. |
| `adbid` | body | `string` | yes | The AnyDB database ID. |
| `adoid` | body | `string` | no | Optional AnyDB record ID for the upload target. |
| `cellpos` | body | `string` | no | Optional AnyDB cell position for the completed upload. |
| `import_content` | body | `boolean` | no | Whether the completed upload should import content. |
| `import_attachto` | body | `string` | no | Optional AnyDB parent ID to attach the imported upload to. |
| `import_templateid` | body | `string` | no | Optional AnyDB template ID for the imported upload. |
| `import_filename` | body | `string` | no | Optional final filename for the completed upload. |
| `import_image` | body | `boolean` | no | Whether the completed upload should be treated as an image. |
