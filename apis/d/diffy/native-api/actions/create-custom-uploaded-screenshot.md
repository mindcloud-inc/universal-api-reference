# Create Custom Uploaded Screenshot with Diffy

Creates a custom uploaded screenshot in Diffy.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:id/create-custom-snapshot`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Create Custom Uploaded Screenshot](https://app.diffy.website/rest)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Project ID. |
| `snapshotName` | body | `string` | yes | Screenshot name |
| `files` | body | `file` | yes | Image file to upload as the custom snapshot. |
| `urls[]` | body | `array<string>` | yes | URLs for uploaded screenshot items |
| `breakpoints[]` | body | `array<number>` | yes | Breakpoints for uploaded screenshot items |
