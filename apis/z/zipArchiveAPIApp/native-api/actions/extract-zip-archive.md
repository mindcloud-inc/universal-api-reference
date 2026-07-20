# Extract ZIP Archive with Zip Archive API app

Extracts a ZIP archive in Zip Archive API app.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.archiveapi.com`
- **Official documentation:** [Extract ZIP Archive](https://archiveapi.com/rest-api/archive-extraction/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | Public URL of the ZIP file to extract. |
| `password` | body | `string` | no | Optional password for encrypted ZIP files. |
