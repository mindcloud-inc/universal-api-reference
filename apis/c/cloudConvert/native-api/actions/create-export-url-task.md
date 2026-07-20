# Create Export URL Task with CloudConvert

Creates an export-by-URL task in CloudConvert.

## Endpoint

- **Method:** `POST`
- **Path:** `/export/url`
- **Base URL:** `https://api.cloudconvert.com/v2`
- **Official documentation:** [Create Export URL Task](https://cloudconvert.com/docs/import-export/export-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<string>` | yes | One or more input task IDs to export. |
| `inline` | body | `boolean` | no | Whether to open the file inline in the browser when possible. |
| `archive_multiple_files` | body | `boolean` | no | Whether to zip multiple exported files into one archive. |
