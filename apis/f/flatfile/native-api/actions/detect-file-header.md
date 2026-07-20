# Detect File Header with Flatfile

Detects the header row in a Flatfile file.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/detect-header`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Detect File Header](https://reference.flatfile.com/api-reference/files/detect-header)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | yes | Sample file data for header detection. |
| `options` | body | `string` | yes | Header detection options. |
