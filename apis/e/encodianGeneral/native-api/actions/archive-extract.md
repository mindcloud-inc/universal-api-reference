# Archive Extract with Encodian - General

Extracts files from a ZIP archive in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/ExtractFromArchive`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Archive Extract](https://support.encodian.com/hc/en-gb/articles/11853992723484)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64-encoded archive file content. |
| `includeFolders` | body | `boolean` | yes | Whether to include folder entries in the extracted output. |
