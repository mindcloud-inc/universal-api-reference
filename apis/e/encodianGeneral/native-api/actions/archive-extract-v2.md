# Archive Extract V2 with Encodian - General

Extracts files from a ZIP archive with Encodian V2.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/ExtractFromArchiveV2`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Archive Extract V2](https://support.encodian.com/hc/en-gb/articles/21005901841564)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64-encoded archive file content. |
| `pathSeparator` | body | `string` | yes | Path separator to use when extracting archive paths. |
| `recursive` | body | `boolean` | yes | Whether to extract nested archives recursively. |
