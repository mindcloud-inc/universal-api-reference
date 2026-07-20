# Create ZIP Archive with Zip Archive API app

Creates a ZIP archive in Zip Archive API app.

## Endpoint

- **Method:** `POST`
- **Path:** `/zip`
- **Base URL:** `https://api.archiveapi.com`
- **Official documentation:** [Create ZIP Archive](https://archiveapi.com/rest-api/file-compression/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files[]` | body | `array<string>` | no | One or more file URLs to include in the ZIP archive. |
| `password` | body | `string` | no | Optional password to protect the ZIP archive. |
| `compressionLevel` | body | `number` | no | Optional ZIP compression level from 1 to 9. |
| `archiveName` | body | `string` | no | Optional output ZIP file name. |
