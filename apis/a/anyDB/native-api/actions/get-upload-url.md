# Get Upload URL with AnyDB

Retrieves a direct upload URL for AnyDB attachments.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integrations/ext/getuploadurl`
- **Base URL:** `https://app.anydb.com`
- **Official documentation:** [Get Upload URL](https://www.anydb.com/openapi/spec.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | query | `string` | yes | The filename to upload. |
| `teamid` | query | `string` | yes | The AnyDB team ID. |
| `adbid` | query | `string` | yes | The AnyDB database ID. |
| `adoid` | query | `string` | yes | The AnyDB record ID. |
| `filesize` | query | `number` | yes | The file size in bytes. |
| `cellpos` | query | `string` | no | Optional AnyDB cell position to upload into. |
| `import_content` | query | `boolean` | no | Whether the uploaded asset should be imported as content. |
| `import_media` | query | `boolean` | no | Whether the uploaded asset should be imported as media. |
